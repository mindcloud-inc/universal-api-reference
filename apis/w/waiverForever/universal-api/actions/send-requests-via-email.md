# WaiverForever: Send Requests via Email

Sends waiver requests by email from WaiverForever.

```
POST https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/send-requests-via-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/send-requests-via-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "replyTo": "sender@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/send-requests-via-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "replyTo": "sender@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailNote` | string | no | Optional note included in the outbound email. |
| `expiresIn` | number | no | Expiration timestamp for the email request. |
| `groupId` | string | yes | Waiver request group to email. |
| `prefillList` | list<object> | no | Recipient objects with `name`, `email`, and optional prefill field values from the request prefill schema. Accepts multiple values as an array. |
| `recipientList` | string | no | Recipient list string for delivery, for example `email<display>`. Use either this field or `Prefill List`. Example: `john@example.com<john@example.com>`. |
| `replyTo` | string | yes | Reply-to email address. Runtime verification showed this account requires a provider-accepted mailbox. Example: `sender@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "trackings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `trackings` | array<object> | Per-recipient waiver request tracking results returned by the email send operation. |

## Native endpoint

Through the native WaiverForever API, this operation is `POST /openapi/v2/waiverRequests/sendGroupEmail` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-requests-via-email.md) for the provider-specific parameters and requirements.

