# Brasil API: List CPTEC Cities

Retrieves CPTEC cities from Brasil API.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-cptec-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-cptec-cities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/list-cptec-cities?${params}`, {
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
      "estado": "string",
      "id": 1,
      "nome": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `estado` | string |  |
| `id` | number |  |
| `nome` | string |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /cptec/v1/cidade` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cptec-cities.md) for the provider-specific parameters and requirements.

