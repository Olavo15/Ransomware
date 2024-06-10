# Descrição do Código de Criptografia e Descriptografia

Este repositório contém um exemplo de código que realiza a criptografia e descriptografia de um arquivo usando a biblioteca `pyaes` em Python. O objetivo deste código é demonstrar como um arquivo pode ser criptografado, armazenado com um novo nome e, posteriormente, descriptografado para recuperar o conteúdo original.

## Criptografia

O processo de criptografia envolve os seguintes passos:

1. **Importação das Bibliotecas**:
    - As bibliotecas `os` e `pyaes` são importadas. `os` é usada para operações de sistema, como remover arquivos, e `pyaes` é usada para criptografia AES.

2. **Leitura do Arquivo Original**:
    - O arquivo original é aberto em modo de leitura binária, seu conteúdo é lido e o arquivo é fechado.

3. **Remoção do Arquivo Original**:
    - Após a leitura, o arquivo original é removido do sistema de arquivos.

4. **Criptografia dos Dados**:
    - Uma chave de criptografia é definida como um valor de bytes.
    - Um objeto AES no modo de operação CTR é criado com a chave.
    - O conteúdo do arquivo é criptografado usando este objeto.

5. **Criação de um Novo Arquivo Criptografado**:
    - O nome do novo arquivo é definido adicionando a extensão `.ransomwaretroll` ao nome original.
    - O novo arquivo é aberto em modo de escrita binária.
    - Os dados criptografados são escritos no novo arquivo, que é então fechado.

## Descriptografia

O processo de descriptografia envolve os seguintes passos:

1. **Importação das Bibliotecas**:
    - As bibliotecas `os` e `pyaes` são importadas novamente.

2. **Leitura do Arquivo Criptografado**:
    - O arquivo criptografado é aberto em modo de leitura binária, seu conteúdo é lido e o arquivo é fechado.

3. **Descriptografia dos Dados**:
    - A mesma chave de criptografia usada para criptografar os dados é utilizada para descriptografá-los.
    - Um objeto AES no modo de operação CTR é criado com a chave.
    - O conteúdo do arquivo criptografado é descriptografado usando este objeto.

4. **Remoção do Arquivo Criptografado**:
    - Após a leitura, o arquivo criptografado é removido do sistema de arquivos.

5. **Criação do Arquivo Original Descriptografado**:
    - Um novo arquivo com o nome original é criado.
    - O conteúdo descriptografado é escrito neste novo arquivo, que é então fechado.

## Conclusão

Este código fornece uma demonstração básica de como usar a biblioteca `pyaes` para criptografar e descriptografar arquivos em Python. É importante notar que, para uso real em aplicações de segurança, a escolha e o gerenciamento das chaves de criptografia devem ser feitos com cuidado para garantir a segurança dos dados.
