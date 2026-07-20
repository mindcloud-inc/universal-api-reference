# Update Contact with eGestor

Updates an existing contact in eGestor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contatos/:codigo`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Update Contact](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L477)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codigo` | path | `number` | yes | Código do contato. |
| `nome` | body | `string` | yes | Nome do contato. Limite 60 caracteres. |
| `tipo[]` | body | `array<string>` | yes | Tipos do contato como lista de strings. Valores documentados: cliente, fornecedor, transportadora. |
| `nomeParaContato` | body | `string` | no | Nome para contato. Limite 60 caracteres. |
| `emails[]` | body | `array<string>` | no | Lista de e-mails do contato. |
| `clienteFinal` | body | `boolean` | no | Define se o contato é cliente final. |
| `obs` | body | `string` | no | Observações gerais do contato. |
