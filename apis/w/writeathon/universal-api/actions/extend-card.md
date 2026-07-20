# Writeathon: Extend Card

Creates a child card under a Writeathon card.

```
POST https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/extend-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Writeathon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/extend-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parent": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/extend-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parent": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parent` | string | yes | The parent card ID to extend. |
| `title` | string | no | Optional title for the new extended card. |
| `content` | string | yes | The content for the new extended card. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `data` | string |  |

## Native endpoint

Through the native Writeathon API, this operation is `POST /v1/users/{{credentials.userId}}/cards/extend` (base URL `https://api.writeathon.cn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extend-card.md) for the provider-specific parameters and requirements.

