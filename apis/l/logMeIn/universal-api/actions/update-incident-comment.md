# LogMeIn: Update Incident Comment

Updates an existing incident comment in LogMeIn.

```
PUT https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/update-incident-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/update-incident-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "referenceNum": "string",
  "commentId": "string",
  "comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/update-incident-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "referenceNum": "string",
    "commentId": "string",
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
| `commentId` | string | yes | Required comment ID. |
| `comment` | string | yes | Updated comment text. |
| `hiddenFromCustomerAt` | date | no | Updated hidden-from-customer timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "hiddenFromCustomerAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `hiddenFromCustomerAt` | date |  |
| `id` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native LogMeIn API, this operation is `PUT /goto-resolve-ticketing/v1/incidents/:referenceNum/comments/:commentId` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-incident-comment.md) for the provider-specific parameters and requirements.

