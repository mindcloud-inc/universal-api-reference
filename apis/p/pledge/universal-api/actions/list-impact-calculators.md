# Pledge: List Impact Calculators

Retrieves impact calculators from Pledge.

```
GET https://connect.mindcloud.co/v1/universal/pledge/latest/actions/list-impact-calculators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pledge `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/list-impact-calculators?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pledge/latest/actions/list-impact-calculators?${params}`, {
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
      "amount": 1,
      "color": "string",
      "createdAt": "string",
      "currencySymbol": "string",
      "description": "string",
      "formula": "string",
      "icon": "string",
      "id": "string",
      "info": "string",
      "name": "Ava Chen",
      "style": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `color` | string |  |
| `createdAt` | string |  |
| `currencySymbol` | string |  |
| `description` | string |  |
| `formula` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `info` | string |  |
| `name` | string |  |
| `style` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Pledge API, this operation is `GET /impact_calculators` (base URL `https://api.pledge.to/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-impact-calculators.md) for the provider-specific parameters and requirements.

