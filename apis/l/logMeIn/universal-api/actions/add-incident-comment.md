# LogMeIn: Add Incident Comment

Creates a new incident comment in LogMeIn.

```
POST https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/add-incident-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/add-incident-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "referenceNum": "string",
  "comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/add-incident-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "referenceNum": "string",
    "comment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `referenceNum` | string | yes | Required incident reference number. |
| `comment` | string | yes | Comment text. |
| `hiddenFromCustomerAt` | date | no | Timestamp marking the comment hidden from customer. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments[]` | array<object> | no | Optional comment attachments. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hiddenFromCustomerAt": "2026-05-07T12:00:00.000Z",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `createdAt` | date |  |
| `hiddenFromCustomerAt` | date |  |
| `id` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `POST /goto-resolve-ticketing/v1/incidents/:referenceNum/comments` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-incident-comment.md) for the provider-specific parameters and requirements.

