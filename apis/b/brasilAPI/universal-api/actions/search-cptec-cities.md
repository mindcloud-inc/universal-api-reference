# Brasil API: Search CPTEC Cities

Finds CPTEC cities in Brasil API by city name.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/search-cptec-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/search-cptec-cities?connectionId=$CONNECTION_ID&cityName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cityName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/search-cptec-cities?${params}`, {
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
| `cityName` | string | yes | The full or partial city name to search. |

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

Through the native Brasil API API, this operation is `GET /cptec/v1/cidade/{cityName}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-cptec-cities.md) for the provider-specific parameters and requirements.

