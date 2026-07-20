# ManyReach: List Sender Errors

Retrieves errors for a sender from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-sender-errors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-sender-errors?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-sender-errors?${params}`, {
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
| `id` | string | yes | The ID of the sender whose errors to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "campaignId": 1,
      "context": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "errorId": 1,
      "followupId": 1,
      "message": "string",
      "senderId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `campaignId` | number |  |
| `context` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `errorId` | number |  |
| `followupId` | number |  |
| `message` | string |  |
| `senderId` | number |  |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/senders/:id/errors` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sender-errors.md) for the provider-specific parameters and requirements.

