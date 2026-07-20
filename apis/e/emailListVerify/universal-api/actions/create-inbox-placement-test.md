# EmailListVerify: Create Inbox Placement Test

Creates an inbox placement test in EmailListVerify.

```
POST https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/create-inbox-placement-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailListVerify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/create-inbox-placement-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/create-inbox-placement-test', {
  method: 'POST',
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
| `name` | string | no | Optional name for the inbox placement test. |
| `webhookUrl` | string | no | Optional HTTP or HTTPS URL to receive placement-test results when complete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emails": [
        "ava@example.com"
      ],
      "id": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Tracking code. |
| `createdAt` | date | Creation timestamp. |
| `emails` | array<string> | Seed email addresses. |
| `id` | string | Placement test ID. |
| `name` | string | Placement test name. |
| `status` | string | Placement test status. |

## Native endpoint

Through the native EmailListVerify API, this operation is `POST /api/inboxPlacementTests` (base URL `https://api.emaillistverify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inbox-placement-test.md) for the provider-specific parameters and requirements.

