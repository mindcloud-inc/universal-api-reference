# Are.na: Update Block

Updates an existing block in Are.na.

```
PUT https://connect.mindcloud.co/v1/universal/are-na/latest/actions/update-block
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/update-block" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/are-na/latest/actions/update-block', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | no | Updated text content for text blocks. |
| `description` | string | no | Updated block description. |
| `id` | string | no | Are.na block ID. |
| `title` | string | no | Updated block title. |

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

Through the native Are.na API, this operation is `PUT blocks/:id` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-block.md) for the provider-specific parameters and requirements.

