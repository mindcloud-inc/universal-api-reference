# Lettr: Schedule Template Email



```
POST https://connect.mindcloud.co/v1/universal/lettr/latest/actions/schedule-template-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/schedule-template-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "scheduledAt": "string",
  "templateSlug": "string",
  "to[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lettr/latest/actions/schedule-template-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "scheduledAt": "string",
    "templateSlug": "string",
    "to[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | Sender email address. |
| `scheduledAt` | string | yes | Scheduled delivery timestamp. |
| `substitutionData` | object | no | Template substitution variables. |
| `templateSlug` | string | yes | Template slug for templated sends. |
| `to[]` | array<string> | yes | Recipient email addresses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accepted": 1,
        "rejected": 1,
        "request_id": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Scheduled email payload. |
| `data.accepted` | number | Accepted recipient count. |
| `data.rejected` | number | Rejected recipient count. |
| `data.request_id` | string | Request ID for the scheduled email. |
| `message` | string | Email schedule status message. |

## Native endpoint

Through the native Lettr API, this operation is `POST /emails/scheduled` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-template-email.md) for the provider-specific parameters and requirements.

