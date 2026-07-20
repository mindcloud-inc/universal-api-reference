# eGestor: List Contacts

Retrieves a list of contacts from eGestor.

```
GET https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGestor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filtro` | string | no | Busca a string informada nos campos nome, fantasia, código, contato, email, telefone e tags. Example: `MindCloud Stage3 Contact 20260401`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endereco` | string | no | Busca a string informada no endereço do contato. Example: `Rua Exemplo`. |
| `telefone` | string | no | Busca o valor informado no campo telefones do contato. Example: `11999999999`. |
| `email` | string | no | Busca o valor informado no campo e-mails do contato. Example: `apps@mindcloud.co`. |
| `clienteFinal` | list | no | Filtra por cliente final. Valores documentados: 1 sim, 2 não. One of: `1`, `2`. Example: `1`. |
| `indIE` | list | no | Filtra por indicador de IE. Valores documentados: 1 contribuinte, 2 isento, 9 não contribuinte. One of: `1`, `2`, `9`. Example: `1`. |
| `IE` | string | no | Filtra por inscrição estadual. Example: `123456`. |
| `IM` | string | no | Filtra por inscrição municipal. Example: `123456`. |
| `suframa` | string | no | Filtra pelo código SUFRAMA. Example: `123456`. |
| `obs` | string | no | Busca a string informada nas observações do contato. Example: `teste`. |
| `fields` | string | no | Campos a retornar separados por vírgula. Example: `codigo,nome,tipo,emails`. |
| `orderBy` | string | no | Ordenação da listagem no formato campo,direção. Example: `nome,asc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "bairro": "string",
          "cep": 1,
          "cidade": "string",
          "clienteFinal": true,
          "codigo": 1,
          "complemento": "string",
          "cpfcnpj": "string",
          "dtCad": "2026-05-07T12:00:00.000Z",
          "dtNasc": "string",
          "emails": [
            "ava@example.com"
          ],
          "fantasia": "string",
          "indicadorIE": 1,
          "inscricaoEstadual": "string",
          "inscricaoMunicipal": "string",
          "logradouro": "string",
          "nome": "string",
          "nomeParaContato": "string",
          "numero": "string",
          "obs": "string",
          "tipo": [
            "string"
          ],
          "uf": "string"
        }
      ],
      "from": 1,
      "lastPage": 1,
      "nextPageUrl": {},
      "perPage": 1,
      "prevPageUrl": {},
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data[].bairro` | string |  |
| `data[].cep` | number |  |
| `data[].cidade` | string |  |
| `data[].clienteFinal` | boolean |  |
| `data[].codigo` | number |  |
| `data[].complemento` | string |  |
| `data[].cpfcnpj` | string |  |
| `data[].dtCad` | date |  |
| `data[].dtNasc` | string |  |
| `data[].emails[]` | string |  |
| `data[].fantasia` | string |  |
| `data[].indicadorIE` | number |  |
| `data[].inscricaoEstadual` | string |  |
| `data[].inscricaoMunicipal` | string |  |
| `data[].logradouro` | string |  |
| `data[].nome` | string |  |
| `data[].nomeParaContato` | string |  |
| `data[].numero` | string |  |
| `data[].obs` | string |  |
| `data[].tipo[]` | string |  |
| `data[].uf` | string |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native eGestor API, this operation is `GET /contatos` (base URL `https://api.egestor.com.br/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

