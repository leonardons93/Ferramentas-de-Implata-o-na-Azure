# Ferramentas-de-Implata-o-na-Azure

Abrir o Cloud Shell
No canto superior direito do portal, clique no ícone do Cloud Shell (parece um terminal ou uma janela de shell).
Você pode escolher entre Bash ou PowerShell. Selecione PowerShell.
. Configurar o Cloud Shell
Se for a primeira vez que você usa o Cloud Shell, será solicitado que você configure um armazenamento. Siga as instruções para criar uma conta de armazenamento, que permitirá armazenar seus arquivos e scripts.
. Executar Comandos
Após a configuração, você pode começar a executar comandos PowerShell diretamente no console do Cloud Shell. Por exemplo, para listar suas máquinas virtuais, você pode usar:

Get-AzVM

teclas de comando na versão web que podemos importa e exporta arquivos troca de cli ou abra a tela em outra aba
. Salvar e Acessar Arquivos
Você pode criar e editar scripts diretamente no Cloud Shell, e os arquivos ficarão disponíveis na sua conta de armazenamento.

 Implantar o Bicep
Para implantar o arquivo Bicep, use o seguinte comando:

az deployment group create --resource-group <nome-do-seu-resource-group> --template-file main.bicep --parameters adminUsername=<seu-usuario> adminPassword=<sua-senha>

6. Verificar a Implantação
Após a implantação, você pode verificar se os recursos foram criados corretamente no Azure Portal ou usando o CLI:


az vm list --resource-group <nome-do-seu-resource-group> --output table
