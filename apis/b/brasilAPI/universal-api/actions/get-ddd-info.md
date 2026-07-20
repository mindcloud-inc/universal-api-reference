# Brasil API: Get DDD Info

Retrieves DDD cities and state information from Brasil API.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-ddd-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-ddd-info?connectionId=$CONNECTION_ID&ddd=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ddd": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-ddd-info?${params}`, {
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
| `ddd` | string | yes | The Brazilian telephone area code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cities": [
        "string"
      ],
      "nome": "string",
      "regiao": {},
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cities` | array<string> |  |
| `nome` | string |  |
| `regiao` | object |  |
| `state` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /ddd/v1/{ddd}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ddd-info.md) for the provider-specific parameters and requirements.

