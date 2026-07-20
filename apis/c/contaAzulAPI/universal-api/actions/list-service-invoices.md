# Conta Azul: List Service Invoices



```
GET https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/list-service-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conta Azul `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/list-service-invoices?connectionId=$CONNECTION_ID&data_competencia_ate=2026-05-07T12%3A00%3A00.000Z&data_competencia_de=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data_competencia_ate": "2026-05-07T12:00:00.000Z",
  "data_competencia_de": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/list-service-invoices?${params}`, {
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
| `data_competencia_ate` | date | yes | Required competence end date. |
| `data_competencia_de` | date | yes | Required competence start date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itens": [
        {}
      ],
      "paginacao": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itens` | array<object> |  |
| `paginacao` | object |  |

## Native endpoint

Through the native Conta Azul API, this operation is `GET /v1/notas-fiscais-servico` (base URL `https://api-v2.contaazul.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-invoices.md) for the provider-specific parameters and requirements.

