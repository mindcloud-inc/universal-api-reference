# Brasil API: Get Address by CEP

Retrieves an address from Brasil API by CEP.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-address-by-cep
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-address-by-cep?connectionId=$CONNECTION_ID&cep=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cep": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-address-by-cep?${params}`, {
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
| `cep` | string | yes | The 8-digit CEP to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cep": "string",
      "city": "string",
      "neighborhood": "string",
      "service": "string",
      "state": "string",
      "street": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cep` | string |  |
| `city` | string |  |
| `neighborhood` | string |  |
| `service` | string |  |
| `state` | string |  |
| `street` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /cep/v1/{cep}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-address-by-cep.md) for the provider-specific parameters and requirements.

