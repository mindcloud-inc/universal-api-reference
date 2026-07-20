# Are.na: Create Block

Creates a new block in Are.na.

```
POST https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-block" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel_ids[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-block', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel_ids[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel_ids[]` | array<number> | yes | Array of channel IDs where the block should be added. |
| `content` | string | no | Text content or URL for the block. |
| `title` | string | no | Optional block title. |
| `value` | string | no | Text, markdown, URL, or other value to create the block from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "content": {},
      "id": 1,
      "source": {},
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `content` | object |  |
| `id` | number |  |
| `source` | object |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Are.na API, this operation is `POST blocks` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-block.md) for the provider-specific parameters and requirements.

