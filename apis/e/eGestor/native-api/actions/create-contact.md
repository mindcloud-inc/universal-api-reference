# Create Contact with eGestor

Creates a new contact in eGestor.

## Endpoint

- **Method:** `POST`
- **Path:** `/contatos`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Create Contact](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L270)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nome` | body | `string` | yes | Nome do contato. Limite 60 caracteres. |
| `tipo[]` | body | `array<string>` | yes | Tipos do contato como lista de strings. Valores documentados: cliente, fornecedor, transportadora. Accepted values: `cliente`, `fornecedor`, `transportadora`. |
| `nomeParaContato` | body | `string` | no | Nome para contato. Limite 60 caracteres. |
| `cpfcnpj` | body | `string` | no | CPF ou CNPJ do contato. |
| `dtNasc` | body | `date` | no | Data de nascimento no formato YYYY-MM-DD. |
| `emails[]` | body | `array<string>` | no | Lista de e-mails do contato. |
| `fones[]` | body | `array<string>` | no | Lista de telefones do contato. |
| `logradouro` | body | `string` | no | Logradouro do contato. |
| `numero` | body | `string` | no | Número do endereço do contato. |
| `codIBGE` | body | `string` | no | Código IBGE da cidade. |
| `uf` | body | `string` | no | UF referente ao código IBGE informado. |
| `clienteFinal` | body | `boolean` | no | Define se o contato é cliente final. |
| `indicadorIE` | body | `list` | no | Indicador de inscrição estadual. Valores documentados: 1 contribuinte, 2 isento, 9 não contribuinte. Accepted values: `1`, `2`, `9`. |
| `obs` | body | `string` | no | Observações gerais do contato. |
| `tags[]` | body | `array<string>` | no | Lista de palavras-chave do contato. |
