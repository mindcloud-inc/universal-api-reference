# GorillaDesk: Create Customer Note

Creates a customer note in GorillaDesk.

```
POST https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/create-customer-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GorillaDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/create-customer-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "customerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/create-customer-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "customerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments[]` | array<file> | no | Accepted file types: image, audio, video, pdf. Limit to 5 files and maximum 10MB per file. |
| `content` | string | yes |  |
| `customerId` | string | yes | Customer Id |
| `notifyUsers[]` | array<string> | no | List of user Ids |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native GorillaDesk API, this operation is `POST /customers/:customerId/notes` (base URL `https://api.gorilladesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-note.md) for the provider-specific parameters and requirements.

