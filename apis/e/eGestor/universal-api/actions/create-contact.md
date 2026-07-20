# eGestor: Create Contact

Creates a new contact in eGestor.

```
POST https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nome": "Kaya Labadie",
  "tipo[]": "cliente"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nome": "Kaya Labadie",
    "tipo[]": "cliente"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nome` | string | yes | Nome do contato. Limite 60 caracteres. Example: `Kaya Labadie`. |
| `tipo[]` | array<string> | yes | Tipos do contato como lista de strings. Valores documentados: cliente, fornecedor, transportadora. One of: `cliente`, `fornecedor`, `transportadora`. Example: `cliente`. |
| `nomeParaContato` | string | no | Nome para contato. Limite 60 caracteres. Example: `Elfrieda Labadie`. |
| `cpfcnpj` | string | no | CPF ou CNPJ do contato. Example: `00000000000191`. |
| `dtNasc` | date | no | Data de nascimento no formato YYYY-MM-DD. Example: `1992-02-13`. |
| `emails[]` | array<string> | no | Lista de e-mails do contato. Example: `exemplo@example.com.br`. |
| `fones[]` | array<string> | no | Lista de telefones do contato. Example: `11999999999`. |
| `logradouro` | string | no | Logradouro do contato. Example: `Rua Exemplo lado ímpar`. |
| `numero` | string | no | Número do endereço do contato. Example: `999`. |
| `codIBGE` | string | no | Código IBGE da cidade. Example: `3550308`. |
| `uf` | string | no | UF referente ao código IBGE informado. Example: `SP`. |
| `clienteFinal` | boolean | no | Define se o contato é cliente final. Example: `true`. |
| `indicadorIE` | list | no | Indicador de inscrição estadual. Valores documentados: 1 contribuinte, 2 isento, 9 não contribuinte. One of: `1`, `2`, `9`. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `obs` | string | no | Observações gerais do contato. Example: `Contato criado pela automação`. |
| `tags[]` | array<string> | no | Lista de palavras-chave do contato. Example: `cliente bom,especial`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codigo": 1,
      "nome": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codigo` | number |  |
| `nome` | string |  |

## Native endpoint

Through the native eGestor API, this operation is `POST /contatos` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

