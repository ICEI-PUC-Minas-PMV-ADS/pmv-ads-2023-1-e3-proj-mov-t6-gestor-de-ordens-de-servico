# Especificações do Projeto

Em um contexto de mundo corporativo cada vez mais conectado e com demandas sendo geradas a todo momento, se mostra útil para o setor de facilities de uma empresa ter uma ferramenta informatizada e disponível online na qual seja possível receber e gerenciar ordens de serviço destinadas ao referido setor. Com base no conhecimento e experiência profissional dos integrantes do grupo, os anseios tanto dos profissionais dos setores de facilities quanto dos usuários foram traduzidos nas histórias das personas apresentadas abaixo. 

## Personas   
![Persona1](https://user-images.githubusercontent.com/76191741/229353765-48c64e18-2dd2-4186-8b3b-4238aaf2fe5c.png)
<br>
<br>
Persona 1: Aline Alves, 39 anos, colaboradora no cargo de Surpevisora de Facility. Aline busca melhores condições para seu crescimento profissional e também deseja melhoria na qualidade e nos dados relacionados aos pedidos no Facility.

Persona 2: Lucas Alexandre, 35 anos, Colaborador no setor de engenharia da empresa, Lucas está motivado em trabalhar no seu crescimento profissional, atuando  nos setores de facility da  empresa. Lucas deseja uma melhor forma de enviar solicitações de OS para mais detalhamento e agilidade nos pedidos.



## Histórias de Usuários

Com base na análise das personas forma identificadas as seguintes histórias de usuários:

|EU COMO... `ALINE ALVES`| QUERO/PRECISO ... `FUNCIONALIDADE`                                   |PARA ... `MOTIVO/VALOR`                                                       |
|------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------|
|Administrador do sistema| Visualizar de maneira mais clara a quantidade de OSs solicitada      | Poder dimensionar os recursos de trabalho                                    |
|Administrador do sistema| Saber o deadline dado pelo solicitante                               | Planejar com antecedencia o cronograma                                       |
|Administrador do sistema| Saber de forma otimizada o escopo a ser trabalhado                   | Pode alocar os recursos com mais facilidade a depender do tipo da atividade  |  
|Administrador do sistema| Saber as datas de criação das OSs                                    | Para poder dar prioridade às mais antigas. Quando possuírem escopos similares|                                       
|Administrador do sistema| Saber a quantidade de solicitações por setor/disciplina e solicitante| Ter a estatística de maiores solicitantes e setores                          |



|EU COMO... `Lucas alexandre`| QUERO/PRECISO ... `FUNCIONALIDADE`              |PARA ... `MOTIVO/VALOR`                                        |
|------------------------|-----------------------------------------------------|---------------------------------------------------------------|
|Cliente    | Agilidade no envio das solicitações                 | O atual processo é inconsistente e não confiável              |
|Cliente    | Especificar data de prazo para o facility           | Para ter o atendimento na data correta: nem antes nem depois  |
|Cliente    | Ter um local único [hub] onde os pedidos são feito  |O processo atual, feitos via e-mail, não são padronizados      |  

## Requisitos

As tabelas que se seguem apresentam os requisitos funcionais e não funcionais que detalham o escopo do projeto.

### Requisitos Funcionais

|ID    | Descrição do Requisito                                                                                                                        |Prioridade|
|------|-----------------------------------------------------------------------------------------------------------------------------------------------|----------|
|RF-001| A aplicação deverá apresentar uma tela onde o usuário poderá fazer login com "Email" e "Senha" e escolher qual tipo de usúario.               |Alta      |
|RF-002| A aplicação deverá apresentar uma tela onde o cliente poderá fazer a solicitação de OS onde haverão campos para informar o escopo de requisição tais como: Descrição, tipo, data , horário e realização da OS.                               |Alta      |
|RF-003| A aplicação deverá exibir uma tela para o Administrador onde ele poderá alterar, editar , excluir e criar ordens de serviços | Média     |
|RF-004| A aplicação deverá exibir uma uma barra de pesquisa na tela de gerenciamento de ordens de serviços para pesquisar as OS's | Média     |
|RF-005| A aplicação deverá exibir uma tela para o administrador criar, deletar, detalhar, e alterar os usuários. | Média     |
 

### Requisitos não Funcionais

|ID     | Descrição do Requisito  |Prioridade |
|-------|-------------------------|----|
|RNF-001| Os dados inseridos pelos usuários na tela de login serão cadastrados no banco de dados.  | ALTA | 
|RNF-002| Os dados das OSs devem mostrar data, hora e situação para o coordenador/administrador. |  MÉDIA | 
|RNF-003| A aplicação web deverá ter disponibilidade em todos os horários. | MÉDIA | 
|RNF-004| A aplicação web deve manter o usuário logado somente por 1 hora. | ALTA |
|RNF-005| A aplicação deve suportar pelo menos dez usuários simultaneamente, e se manter disponível 24/7. | MÉDIA |



## Restrições

O projeto está restrito pelos itens apresentados na tabela a seguir.

|ID| Restrição                                             |
|--|-------------------------------------------------------|
|01| O projeto deverá ser interativo.                      |            
|02| Desenvolver a aplicação Web atendendo às necessidades de OSs dos facilities, respeitando as respectivas fases do projeto. |
|02| Número de controles não pode ser maior do que 10 por tela. |
|02| A equipe de desenvolvimento terá de jornada de trabalho das 07:30 até 16:30 |
|02| A aplicação web terá prazo de manutenção de 3 meses após a entrega, incluído no valor. Após isso, a manutenção passa a ter cobrança vinculada.   |  



## Diagrama de Casos de Uso

O diagrama de casos de uso é o próximo passo após a elicitação de requisitos, que utiliza um modelo gráfico e uma tabela com as descrições sucintas dos casos de uso e dos atores. Ele contempla a fronteira do sistema e o detalhamento dos requisitos funcionais com a indicação dos atores, casos de uso e seus relacionamentos. 

![DiagramaClassesGestorOs](https://user-images.githubusercontent.com/76191741/229353789-ad7680a1-d769-40bb-9460-690a275ce028.png)

