# AvoSMS: Update SMS Template

Updates an existing SMS template in AvoSMS.

```
PUT https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/update-sms-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AvoSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/update-sms-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelId": "69cc2dbd29f21",
  "modelName": "MindCloud Template Updated",
  "modelContent": "MindCloud stage 3 test updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/update-sms-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelId": "69cc2dbd29f21",
    "modelName": "MindCloud Template Updated",
    "modelContent": "MindCloud stage 3 test updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelId` | string | yes | SMS template ID Example: `69cc2dbd29f21`. |
| `modelName` | string | yes | SMS template name Example: `MindCloud Template Updated`. |
| `modelContent` | string | yes | SMS template content Example: `MindCloud stage 3 test updated`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AvoSMS API returns.

## Native endpoint

Through the native AvoSMS API, this operation is `POST /v1/model/sms/update` (base URL `https://api.avosms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sms-template.md) for the provider-specific parameters and requirements.

