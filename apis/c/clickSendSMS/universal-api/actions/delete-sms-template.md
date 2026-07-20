# ClickSend SMS: Delete SMS Template

Deletes an existing SMS template from ClickSend SMS.

```
DELETE https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/delete-sms-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/delete-sms-template?connectionId=$CONNECTION_ID&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/delete-sms-template?${params}`, {
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
| `template_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "httpCode": 1,
      "responseCode": "string",
      "responseMsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `httpCode` | number |  |
| `responseCode` | string |  |
| `responseMsg` | string |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `DELETE /v3/sms/templates/:template_id` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sms-template.md) for the provider-specific parameters and requirements.

