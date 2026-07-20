# ClickSend SMS: Update SMS Template

Updates an existing SMS template in ClickSend SMS.

```
PUT https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/update-sms-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/update-sms-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/update-sms-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template_id` | string | yes |  |
| `template_name` | string | no |  |
| `body` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "templateId": 1,
      "templateName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `templateId` | number |  |
| `templateName` | string |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `PUT /v3/sms/templates/:template_id` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sms-template.md) for the provider-specific parameters and requirements.

