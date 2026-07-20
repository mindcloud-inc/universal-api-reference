# AvoSMS: Delete SMS Template

Deletes an existing SMS template from AvoSMS.

```
DELETE https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/delete-sms-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AvoSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/delete-sms-template?connectionId=$CONNECTION_ID&modelId=69cc2dbd29f21" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "69cc2dbd29f21"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/delete-sms-template?${params}`, {
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
| `modelId` | string | yes | SMS template ID Example: `69cc2dbd29f21`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AvoSMS API returns.

## Native endpoint

Through the native AvoSMS API, this operation is `POST /v1/model/sms/delete` (base URL `https://api.avosms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sms-template.md) for the provider-specific parameters and requirements.

