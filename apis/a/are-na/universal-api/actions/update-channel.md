# Are.na: Update Channel

Updates an existing channel in Are.na.

```
PUT https://connect.mindcloud.co/v1/universal/are-na/latest/actions/update-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/update-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/are-na/latest/actions/update-channel', {
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
| `description` | string | no | Updated markdown description. |
| `id` | string | no | Are.na channel ID or slug. |
| `title` | string | no | Updated channel title. |
| `visibility` | string | no | Updated visibility: public, closed, or private. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "counts": {},
      "description": {},
      "id": 1,
      "slug": "string",
      "title": "string",
      "type": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `counts` | object |  |
| `description` | object |  |
| `id` | number |  |
| `slug` | string |  |
| `title` | string |  |
| `type` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Are.na API, this operation is `PUT channels/:id` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel.md) for the provider-specific parameters and requirements.

