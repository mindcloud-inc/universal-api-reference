# Conta Azul: Get Invoice By Key



```
GET https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-invoice-by-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conta Azul `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-invoice-by-key?connectionId=$CONNECTION_ID&chave=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chave": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contaAzulAPI/latest/actions/get-invoice-by-key?${params}`, {
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
| `chave` | string | yes | Conta Azul invoice key from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chave": "string",
      "data_emissao": "2026-05-07T12:00:00.000Z",
      "numero": "string",
      "situacao": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chave` | string |  |
| `data_emissao` | date |  |
| `numero` | string |  |
| `situacao` | string |  |

## Native endpoint

Through the native Conta Azul API, this operation is `GET /v1/notas-fiscais/{chave}` (base URL `https://api-v2.contaazul.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-by-key.md) for the provider-specific parameters and requirements.

