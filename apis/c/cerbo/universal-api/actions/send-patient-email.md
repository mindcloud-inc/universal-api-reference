# Cerbo: Send Patient Email

Sends an email to a Cerbo patient.

```
PUT https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/send-patient-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/send-patient-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "patient_id": 1,
  "subject": "string",
  "body": "string",
  "reply-to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/send-patient-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "patient_id": 1,
    "subject": "string",
    "body": "string",
    "reply-to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient_id` | number | yes | ID of the patient to send email to |
| `subject` | string | yes | Subject of email to be sent |
| `body` | string | yes | Body of email to be sent |
| `reply-to` | string | yes | This is the address that any patient response will be forwarded to (the email itself will be sent from do-not-reply@md-hq.com). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /patients/:patient_id/emails/send` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-patient-email.md) for the provider-specific parameters and requirements.

