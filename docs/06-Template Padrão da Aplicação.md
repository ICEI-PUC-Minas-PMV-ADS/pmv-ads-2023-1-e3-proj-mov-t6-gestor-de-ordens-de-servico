# Tela Padrão da Aplicação - Gestor de Ordem de Serviços [OS]

## Tela de apresentação

##### É apresentado ao usuário uma tela de "Bem Vindo" do aplicativo.

> Aspecto Visual
> ![Tela 1](https://user-images.githubusercontent.com/76191741/236713740-a27a0292-e5c0-4bfb-9149-0fbf43ff0bdd.JPG)

> Artefato de Construção

 import React from 'react';
import { StyleSheet, Text, View, Image, Button } from 'react-native';

const WelcomePage = () => {
  return (
    <View style={styles.container}>
      <Image source={require('./gtos-logo.png')} style={styles.logo} />
      <Text style={styles.title}>Bem-vindo(a) ao GTOS</Text>
      <Text style={styles.subtitle}>Gestor de Ordens de Serviço</Text>
      <Text style={styles.subtitlee}>Espero que você goste da experiência.</Text>
      <Text style={styles.title}></Text>
      <Button 
    title='Acessar'
    onPress={() => {navigation.navigate('LoginScreen')}}
    />
    </View>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#B9C9F8',
  },
  logo: {
    width: 150,
    height: 150,
    marginBottom: 20,
  },
  title: {
    fontSize: 24,
    fontWeight: 'bold',
    textAlign: 'center',
    marginBottom: 10,
    color: 'blue',
  },
  subtitle: {
    fontSize: 20,
    textAlign: 'center',
    marginHorizontal: 40,
    color: '#0139D3',
  },

  subtitlee: {
    fontSize: 13,
    textAlign: 'center',
    marginHorizontal: 40,
    color: '#1B4B97',
  },
});

export default WelcomePage;
  
## Tela de Principal

##### Para requisito de funcionalidade é requerido uma tela de login que permita do usuário cliente. Com controles de Email, Senha e Botão de ação - com cadastro a priori.

> Aspecto Visual
  ![tela 2](https://user-images.githubusercontent.com/76191741/236714092-873db82c-f233-47eb-9c9a-651be8913c2e.JPG)

> Artefato de Construção
  
  import React, { useState } from 'react';
import { View, Text, TextInput, TouchableOpacity, StyleSheet, Image } from 'react-native';

const LoginScreen = () => {
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');

  const handleLogin = () => {
    // implementar a lógica de login aqui
  };

  return (
    <View style={styles.container}>
      <Image style={styles.logo} source={require('./gtos.png')} />
      <Text style={styles.heading}></Text>
      <Text style={styles.heading}>Login</Text>

      <TextInput
        style={styles.input}
        placeholder="Digite seu e-mail"
        value={email}
        onChangeText={(text) => setEmail(text)}
      />

      <TextInput
        style={styles.input}
        placeholder="Digite sua senha"
        secureTextEntry={true}
        value={password}
        onChangeText={(text) => setPassword(text)}
      />

      <TouchableOpacity style={styles.button} onPress={handleLogin}>
        <Text style={styles.buttonText} onPress={() => {navigation.navigate('Logoninitial')}} >Entrar</Text>
      </TouchableOpacity>
    <Text style={styles.heading}></Text>

      <Text style={styles.cadastro} onPress={() => {navigation.navigate('Register')}}>Não é cadastrado? Inscrever-se</Text>

    </View>
  );
};


const styles = StyleSheet.create({
  logo: {
    height: 200,
    width: 200,
  },
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#F5FCFF',
  },
  heading: {
    fontSize: 24,
    marginBottom: 30,
    fontWeight: 'bold',
    color: 'blue',
  },
  input: {
    width: '80%',
    padding: 10,
    marginBottom: 20,
    backgroundColor: '#FFF',
    borderRadius: 5,
    borderWidth: 1,
    borderColor: '#CCC',
  },
  button: {
    width: '80%',
    padding: 10,
    backgroundColor: '#3498DB',
    alignItems: 'center',
    borderRadius: 5,
  },
  buttonText: {
    color: '#FFF',
    fontSize: 16,
  },
  cadastro:{
    color: 'blue',
    textDecorationLine: 'underline',
  }
});

export default LoginScreen;

## Tela de Criação de Usuário

##### Requisito gerador da funcionalidade, o usuário ao clicar em "Não é cadastrado? Inscrever-se" é levada a uma tela de cadastro de novo usuário.
        
> Aspecto Visual
![Tela 3](https://user-images.githubusercontent.com/76191741/236714346-3a42d9da-e4bb-4bc2-8da6-27b1e7f3096b.JPG)
        
> Artefato de Construção

 import React, { useState } from 'react';
import { View, Text, TextInput, TouchableOpacity, StyleSheet, Image, CheckBox } from 'react-native';

const Register = () => {
  const [email, setEmail] = useState('');
  const [nome, setNome] = useState('');
  const [password, setPassword] = useState('');
  const [cpf, setCpf] = useState('');
  const [isSelected, setSelection] = useState('');

  
  const handleCpfChange = (text) => {
    let formattedCpf = text.replace(/\D/g, '');
    formattedCpf = formattedCpf.substring(0, 11);
    formattedCpf = formattedCpf.replace(/(\d{3})(\d{3})(\d{3})/, '$1.$2.$3-');
    setCpf(formattedCpf);
  };

  return (
    <View style={styles.container}>
      <Image style={styles.logo} source={require('./gtos.png')} />
      <Text style={styles.heading}></Text>
      <Text style={styles.heading}>Cadastrar-se</Text>

      <TextInput
        style={styles.input}
        placeholder="Digite seu nome"
        value={nome}
        onChangeText={(text) => setNome(text)}
      />

      <TextInput
      style={styles.input}
        placeholder="Digite seu email"
        value={nome}
        onChangeText={(text) => setNome(text)}
      />

      <TextInput
      style={styles.input}
        value={cpf}
        placeholder="Digite seu CPF"
        onChangeText={handleCpfChange}
        keyboardType="numeric"
        maxLength={11}
      />

      <TextInput
        style={styles.input}
        placeholder="Digite sua senha"
        secureTextEntry={true}
        value={password}
        onChangeText={(text) => setPassword(text)}
      />
      
      <CheckBox
        value={isSelected}
        onValueChange={setSelection}
      />
      <Text>{isSelected ? 'Eu aceito os termos de uso' : 'Eu não aceito os termos de uso'}</Text>
      <Text style={styles.heading}></Text>
      <TouchableOpacity style={styles.button} onPress={() => navigation.navigate('')}>
        <Text style={styles.buttonText}> Criar conta</Text>
      </TouchableOpacity>
    <Text style={styles.heading}></Text>

    </View>
  );
};


const styles = StyleSheet.create({
  logo: {
    height: 100,
    width: 100,
  },
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#F5FCFF',
  },
  heading: {
    fontSize: 24,
    marginBottom: 30,
    fontWeight: 'bold',
    color: 'blue',
  },
  input: {
    width: '80%',
    padding: 10,
    marginBottom: 20,
    backgroundColor: '#FFF',
    borderRadius: 5,
    borderWidth: 1,
    borderColor: '#CCC',
  },
  button: {
    width: '80%',
    padding: 10,
    backgroundColor: '#3498DB',
    alignItems: 'center',
    borderRadius: 5,
  },
  buttonText: {
    color: '#FFF',
    fontSize: 16,
  },

});

export default Register;

