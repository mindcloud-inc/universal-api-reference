# EmailListVerify: Get Inbox Placement Test

Retrieves inbox placement test status and results from EmailListVerify.

```
GET https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-inbox-placement-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailListVerify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-inbox-placement-test?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/get-inbox-placement-test?${params}`, {
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
| `code` | string | yes | Inbox placement test tracking code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "recipients": {
        "email": "ava@example.com",
        "esp": "string",
        "placement": "string",
        "type": "string"
      },
      "sender": "ava@example.com",
      "status": "string",
      "summary": {
        "inbox": 1,
        "missing": 1,
        "promotions": 1,
        "spam": 1,
        "waiting": 1
      },
      "updatedAt": "2026-05-07T12:00:00.000Z"
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
| `name` | string | Placement test name. |
| `recipients` | array<object> | Seed recipients and placements. |
| `recipients.email` | string | Seed recipient email. |
| `recipients.esp` | string | Email service provider. |
| `recipients.placement` | string | Detected placement. |
| `recipients.type` | string | Seed mailbox type. |
| `sender` | string | Detected sender email. |
| `status` | string | Placement test status. |
| `summary` | object | Placement summary percentages. |
| `summary.inbox` | number | Inbox percentage. |
| `summary.missing` | number | Missing percentage. |
| `summary.promotions` | number | Promotions percentage. |
| `summary.spam` | number | Spam percentage. |
| `summary.waiting` | number | Waiting percentage. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native EmailListVerify API, this operation is `GET /api/inboxPlacementTests/:code` (base URL `https://api.emaillistverify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox-placement-test.md) for the provider-specific parameters and requirements.

