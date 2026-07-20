# OTO: List Available Cities

Retrieves available cities from the OTO API.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-available-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-available-cities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-available-cities?${params}`, {
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
| `limit` | number | no | Maximum number of available cities to return. Default: `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limit": 1,
      "orders": [
        {}
      ],
      "page": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number |  |
| `orders` | array<object> |  |
| `page` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native OTO API, this operation is `POST /availableCities` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-cities.md) for the provider-specific parameters and requirements.

