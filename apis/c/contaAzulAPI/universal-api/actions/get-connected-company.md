# Conta Azul: Get Connected Company



```
GET https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-connected-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conta Azul `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-connected-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-connected-company?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "dataFundacao": "2026-05-07T12:00:00.000Z",
      "documento": "string",
      "email": "ava@example.com",
      "nomeFantasia": "string",
      "razaoSocial": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataFundacao` | date | Founding date of the connected company. |
| `documento` | string | Brazilian company document number (CNPJ). |
| `email` | string | Primary company email address. |
| `nomeFantasia` | string | Trade name of the connected company. |
| `razaoSocial` | string | Registered legal name of the connected company. |

## Native endpoint

Through the native Conta Azul API, this operation is `GET /v1/pessoas/conta-conectada` (base URL `https://api-v2.contaazul.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connected-company.md) for the provider-specific parameters and requirements.

