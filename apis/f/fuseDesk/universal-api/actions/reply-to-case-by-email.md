# FuseDesk: Reply to Case by Email

Sends an email reply for an existing FuseDesk case.

```
POST https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/reply-to-case-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/reply-to-case-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "caseId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/reply-to-case-by-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "caseId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bcc` | string | no | Comma-separated BCC recipient addresses. |
| `body` | string | yes | Plain-text reply body. |
| `caseId` | number | yes | The FuseDesk case ID to reply to. |
| `cc` | string | no | Comma-separated CC recipient addresses. |
| `from` | string | no | Sender email address. |
| `html` | string | no | HTML reply body. |
| `templateId` | number | no | Optional FuseDesk email template ID. |
| `to` | string | no | Recipient email address. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FuseDesk API returns.

## Native endpoint

Through the native FuseDesk API, this operation is `POST /api/v1/cases/:caseId/reply` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reply-to-case-by-email.md) for the provider-specific parameters and requirements.

