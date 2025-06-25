
# Implementando um Monitoramento no Azure

## Configurando o Alerta

Ao criar um novo recurso no Azure, você precisa seguir o principio de observabilidade do seu ambiente, para identificar padrões, comportamentos, metricas e consequentemente gerar alertas que te auxiliarão na identificação de pontos de falha e mantendo a alta disponibilidade do seus serviços.

No campo de pesquisa, procure por Monitor. Voce vai entrar no recursos

## Monitor

O recurso de monitor disponivel no Azure te fornece uma central de administração completa para monitorar todos os aspectos do seu ecosistema na nuvem. 

O primeiro passo é a criação do habilitar o agent para coletar os dados da VM. aqui por exemplo, uma VM.

**1º** Habilitar o agent na maquina destino. Navegue pelo meno do lado esquerdo da tela, até a opção "Insights > Virtual Machines" eSelecione a opção "Overview" na barra superior, como na imagem abaixo.

![image](https://github.com/RafBaeta/AZ-104/blob/122344fe96738ca0f533be5a3f6a58013bbb17bf/Implementando%20Monitoramento%20no%20Azure/images/1%20Habilitar%20Agent.png)

**2º** Criar uma Regra de alerta (Alert Rule) 

![image](https://github.com/RafBaeta/AZ-104/blob/122344fe96738ca0f533be5a3f6a58013bbb17bf/Implementando%20Monitoramento%20no%20Azure/images/2.0%20Alert%20Rule.png)

  **2.1** Clique em "Select Scope" para selecionar o ativo que voce procura, procure pela sua Maquina Virtual (Ou recurso que queira adicionar)
  
  ![image](https://github.com/RafBaeta/AZ-104/blob/122344fe96738ca0f533be5a3f6a58013bbb17bf/Implementando%20Monitoramento%20no%20Azure/images/2.1%20Selecione%20um%20escopo.png)

 **2.2** Apos Selecionar, Em "Condition" procure o item que voce quer que dispare o alerta. Aqui vou selecionar a quantidade de memoria disponivel.
  
  ![image](https://github.com/user-attachments/assets/c5c260dd-8deb-4edf-a702-a0dd91276969)

  **2.3** Faça os ajustes conforme voce queira que a logica funcione. Por exemplo, abaixo escolhi que minha VM disparará o alarme apos ter menos de 140MB de RAM disponivel em média.

  ![image](https://github.com/user-attachments/assets/855f41d3-d184-4ec7-8935-563fa62ea2c1)

  **2.4** Selecione a Ação que voce quer tomar, neste caso o Action Group. Que já tenho criado aqui com a ação de enviar email. Caso ainda nao tenha uma Action Group Criada, voce pode criar um clicando em "Create action group"

  ![image](https://github.com/user-attachments/assets/83b90316-56ff-4f3b-82d4-8f5112ce8dde)

  **2.5** Selecione os detalhes do alerta, como a Severidade que voce julga ter, o nome da Regra, a Descrição. Faça da melhor forma que torne o alerta util.

  **2.6** Selecione as Tags conforme seu ambiente necessite/exija

  **2.7** Finalize: Em "Review + Create" fica um resumo completo de tudo que voce selecionou e vai aplicar na sua regra de alerta.

 ![image](https://github.com/RafBaeta/AZ-104/blob/a5f3bfb9649d12fa1c4d9d3983dd2d176b51bc6f/Implementando%20Monitoramento%20no%20Azure/images/2.7%20Review%20e%20Create.png)

**Pronto!! Assim que alguma das suas regras forem atingidas, voce recebera um alerta como esse abaixo.**

 ![image](https://github.com/RafBaeta/AZ-104/blob/122344fe96738ca0f533be5a3f6a58013bbb17bf/Implementando%20Monitoramento%20no%20Azure/images/Alerta%20disparado.png)

