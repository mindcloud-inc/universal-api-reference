# UpGuard: Send Security Questionnaire To Vendor

Sends a security questionnaire to a vendor in UpGuard.

```
POST https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/send-security-questionnaire-to-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/send-security-questionnaire-to-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "questionnaireTypeId": 1,
  "senderEmail": "ava@example.com",
  "dueDate": "string",
  "recipients[]": [
    {}
  ],
  "riskInformationVisibility": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/send-security-questionnaire-to-vendor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "questionnaireTypeId": 1,
    "senderEmail": "ava@example.com",
    "dueDate": "string",
    "recipients[]": [{}],
    "riskInformationVisibility": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailMessage` | string | no | Optional questionnaire email message. |
| `emailTitle` | string | no | Optional questionnaire email title. |
| `questionnaireTypeId` | number | yes | The numeric ID of the questionnaire type to send. |
| `reminderDate` | string | no | Optional future ISO 8601 reminder date. |
| `senderEmail` | string | yes | The email address of the questionnaire sender. |
| `dueDate` | string | yes | The future ISO 8601 due date for the questionnaire. |
| `recipients[]` | array<object> | yes | The list of questionnaire recipients. |
| `riskInformationVisibility` | string | yes | The visibility level of risk information in the questionnaire. |
| `vendorPrimaryHostname` | string | no | The primary hostname of the vendor to which the questionnaire will be sent. |
| `vendorId` | number | no | The vendor ID to which the questionnaire will be sent. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UpGuard API returns.

## Native endpoint

Through the native UpGuard API, this operation is `POST /vendor/questionnaire` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-security-questionnaire-to-vendor.md) for the provider-specific parameters and requirements.

