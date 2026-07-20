# Raindrop: Merge Collections



```
PUT https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/merge-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/merge-collections" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ids[]": [
    1
  ],
  "to": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/merge-collections', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ids[]": [1],
    "to": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids[]` | array<number> | yes | Array of collection IDs to merge from. |
| `to` | number | yes | Collection ID to merge into. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ids": [
        1
      ],
      "modified": 1,
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ids` | array<number> |  |
| `modified` | number |  |
| `result` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `PUT /collections/merge` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-collections.md) for the provider-specific parameters and requirements.

