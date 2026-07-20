# Writeathon: Create Card With Attachments

Creates a new Writeathon card with attachments.

```
POST https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/create-card-with-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Writeathon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/create-card-with-attachments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "attachments": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/writeathon/latest/actions/create-card-with-attachments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "attachments": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Optional card title. If omitted, Writeathon creates one automatically. |
| `content` | string | yes | The card content to save in Writeathon. |
| `attachments` | string | yes | A JSON-array string of Writeathon attachments. Example: [{"type":"link","title":"Example","url":"https://example.com"}] |
| `space` | string | no | Optional Writeathon space ID. Leave blank to use the default space. |

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

Through the native Writeathon API, this operation is `POST /v1/users/{{credentials.userId}}/cards` (base URL `https://api.writeathon.cn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-card-with-attachments.md) for the provider-specific parameters and requirements.

