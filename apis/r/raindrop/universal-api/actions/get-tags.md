# Raindrop: Get Tags



```
GET https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-tags?${params}`, {
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
| `collectionId` | string | no | Collection ID. Use 0 for all raindrops except Trash. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "_id": "string",
          "count": 1
        }
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[]._id` | string |  |
| `items[].count` | number |  |
| `result` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `GET /tags/:collectionId` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tags.md) for the provider-specific parameters and requirements.

