# Conta Azul: Search Accounts Payable



```
GET https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/search-accounts-payable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conta Azul `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/search-accounts-payable?connectionId=$CONNECTION_ID&data_vencimento_ate=2026-05-07T12%3A00%3A00.000Z&data_vencimento_de=2026-05-07T12%3A00%3A00.000Z&pagina=1&tamanho_pagina=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data_vencimento_ate": "2026-05-07T12:00:00.000Z",
  "data_vencimento_de": "2026-05-07T12:00:00.000Z",
  "pagina": "1",
  "tamanho_pagina": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/search-accounts-payable?${params}`, {
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
| `data_vencimento_ate` | date | yes | Required upper due-date bound. |
| `data_vencimento_de` | date | yes | Required lower due-date bound. |
| `pagina` | number | yes | Page number required by Conta Azul. |
| `tamanho_pagina` | number | yes | Page size required by Conta Azul. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itens": [
        {}
      ],
      "itens_totais": 1,
      "totais": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itens` | array<object> |  |
| `itens_totais` | number |  |
| `totais` | object |  |

## Native endpoint

Through the native Conta Azul API, this operation is `GET /v1/financeiro/eventos-financeiros/contas-a-pagar/buscar` (base URL `https://api-v2.contaazul.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-accounts-payable.md) for the provider-specific parameters and requirements.

