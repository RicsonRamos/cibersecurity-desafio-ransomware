# Criptografia de Arquivo com AES (Ransomware Simulado)

Este projeto simula o comportamento de um **ransomware**, utilizando a criptografia **AES no modo CTR** (Counter) para criptografar arquivos e salvá-los com uma nova extensão. O arquivo original é removido após a criptografia, tornando o conteúdo inacessível sem a chave adequada.

**Aviso**: Este código **não deve ser usado de forma maliciosa**. Ele foi criado com fins educativos para demonstrar como a criptografia e a manipulação de arquivos podem ser feitas com o algoritmo AES.

## Descrição

Este script realiza as seguintes ações:
1. Lê um arquivo de texto (exemplo: `file.txt`).
2. Apaga o arquivo original.
3. Criptografa o conteúdo do arquivo utilizando o **algoritmo AES (Advanced Encryption Standard)** no modo **CTR**.
4. Cria um novo arquivo com a extensão `.ransomwaretroll` contendo os dados criptografados.
5. O arquivo original é **removido permanentemente**, e o arquivo criptografado substitui o original.

Este tipo de comportamento é frequentemente associado a **ransomware**, que é um tipo de malware que criptografa arquivos em um computador e exige pagamento para a recuperação dos dados.

## Requisitos

Para executar este código, você precisará de:
- **Python 3.x** instalado.
- A biblioteca `pyaes` para criptografia AES. Ela pode ser instalada via pip:
  ```bash
  pip install pyaes
  ```

## Como Usar

1. **Clone o repositório**:

   Se você ainda não fez o download do repositório, clone-o com o comando:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-repositorio.git
   cd nome-do-repositorio
   ```

2. **Prepare o arquivo**:
   - Coloque o arquivo de texto que deseja criptografar no mesmo diretório do script ou modifique o caminho do arquivo no código.

3. **Execute o script**:
   Execute o código Python no seu terminal:
   ```bash
   python criptografar.py
   ```
   **Atenção**: Após a execução, o arquivo original será apagado e será criado um arquivo criptografado com a extensão `.ransomwaretroll`.

## Exemplo

Se o arquivo de entrada for `file.txt` e seu conteúdo for:
```
Olá, isso é um arquivo de teste.
```

Após a execução do código, o arquivo `file.txt` será removido, e um novo arquivo `file.txt.ransomwaretroll` será gerado com os dados criptografados.

## Explicação do Código

1. **Leitura do arquivo**:
   O arquivo a ser criptografado é aberto e seu conteúdo é lido como dados binários.

2. **Remoção do arquivo original**:
   O arquivo original é removido logo após a leitura, de forma que não há backup dos dados originais.

3. **Criptografia AES**:
   O algoritmo **AES no modo CTR** é utilizado para criptografar os dados. A chave usada para a criptografia é a string `testeransomwares` (note que em uma aplicação real, a chave deve ser mantida de forma segura e não hardcoded).

4. **Criação do arquivo criptografado**:
   O arquivo criptografado é salvo com a extensão `.ransomwaretroll`.

## Considerações de Segurança

- **Perda de dados**: O arquivo original é removido sem backup, o que pode resultar na **perda permanente** dos dados se o arquivo criptografado não puder ser recuperado.
- **Uso educacional**: Este projeto é destinado a fins educativos para demonstrar como a criptografia funciona. **Não use este código para atividades maliciosas**.
- **Segurança da chave**: Em um ambiente real, a chave de criptografia deve ser armazenada de forma segura e não deve ser fixada no código-fonte. Técnicas como **gerenciamento seguro de chaves** e **criptografia de chave pública/privada** são recomendadas.

## Contribuições

Contribuições são bem-vindas! Se você deseja melhorar ou corrigir este projeto, fique à vontade para enviar **pull requests**.

## Licença

Este projeto está licenciado sob a **Licença MIT**. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Esse **README** fornece uma explicação detalhada do funcionamento do código e das precauções de segurança, além de fornecer instruções para executar o script e informações sobre a finalidade do projeto.
