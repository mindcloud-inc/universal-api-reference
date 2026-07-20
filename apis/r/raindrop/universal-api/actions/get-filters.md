# Raindrop: Get Filters



```
GET https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-filters?${params}`, {
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
      "collectionId": 1,
      "created": [
        {}
      ],
      "result": true,
      "tags": [
        {
          "_id": "string",
          "count": 1
        }
      ],
      "types": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collectionId` | number |  |
| `created` | array<object> |  |
| `result` | boolean |  |
| `tags` | array<object> |  |
| `tags[]._id` | string |  |
| `tags[].count` | number |  |
| `types` | array<object> |  |

## Native endpoint

Through the native Raindrop API, this operation is `GET /filters/:collectionId` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-filters.md) for the provider-specific parameters and requirements.

