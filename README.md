# Script de Busca e Download de Arquivo

Este script em Bash permite que o usuário selecione um servidor remoto, execute uma busca por um arquivo específico nesse servidor e faça o download do arquivo, caso ele seja encontrado.

## Requisitos

- Sistema operacional Linux
- Chave SSH privada para acesso aos servidores remotos
- Conexão com a internet

## Como utilizar

1. Baixe e salve o script em um diretório de sua preferência com o nome `search_and_download.sh`
2. Abra o terminal e navegue até o diretório onde o arquivo foi salvo
3. Digite o seguinte comando no terminal: `chmod +x search_and_download.sh` para conceder permissão de execução ao arquivo
4. Digite o seguinte comando no terminal: `./search_and_download.sh` para executar o script
5. Siga as instruções exibidas na tela para selecionar um servidor remoto, buscar e fazer o download do arquivo

## Passo a passo

1. O script define o caminho para a pasta de busca em `destination_folder`.
2. A pasta de busca é criada caso ela não exista.
3. O script lista as chaves disponíveis na pasta `.ssh` e pergunta ao usuário qual delas usar.
4. O script define os IPs dos servidores em um array associativo `servers`.
5. O script exibe a lista de servidores e pergunta ao usuário para selecionar um.
6. O script pergunta ao usuário para inserir o nome do arquivo que deseja buscar.
7. O script define o comando de busca de arquivo, utilizando o comando `find` do Linux.
8. O comando é executado e a saída é capturada na variável `output`.
9. O script verifica se o arquivo foi encontrado na saída capturada.
10. Se o arquivo foi encontrado, o script pergunta ao usuário se ele deseja fazer o download do arquivo.
11. Se o usuário confirmar o download, o script copia o arquivo para a pasta de destino, converte o arquivo para `.zip` e exclui o arquivo original.
12. Se o arquivo não for encontrado, o script exibe uma mensagem informando que o arquivo não foi encontrado.

## Código

O código do script está em Bash e pode ser encontrado no arquivo `search_and_download.sh`.
