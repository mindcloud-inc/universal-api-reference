# Syften: List Items

Retrieves matching mention items from Syften.

```
GET https://connect.mindcloud.co/v1/universal/syften/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syften `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syften/latest/actions/list-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syften/latest/actions/list-items?${params}`, {
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
| `limit` | number | no | Maximum number of items to return |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filter": "string",
      "id": "string",
      "item": {},
      "matched_on": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filter` | string |  |
| `id` | string |  |
| `item` | object |  |
| `matched_on` | date |  |

## Native endpoint

Through the native Syften API, this operation is `POST /api/0.0/items/get` (base URL `https://syften.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

