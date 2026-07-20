# Weekdone: Search Items

Finds items in Weekdone.

```
GET https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/search-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weekdone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/search-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/search-items?${params}`, {
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
| `period` | string | no |  |
| `teamId` | number | no |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Weekdone API, this operation is `GET items` (base URL `https://api.weekdone.com/1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-items.md) for the provider-specific parameters and requirements.

