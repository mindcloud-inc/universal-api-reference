# Abbyy: Process Fields

Processes multiple fields in ABBYY Cloud OCR SDK.

```
PUT https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/process-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abbyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/process-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "settingsXml": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/process-fields', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "settingsXml": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | ABBYY OCR task identifier created by Submit Image. |
| `settingsXml` | string | yes | ABBYY field-definition XML payload that describes the coordinates and field ids to recognize. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Abbyy API returns.

## Native endpoint

Through the native Abbyy API, this operation is `POST /v2/processFields` (base URL `https://cloud-westus.ocrsdk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-fields.md) for the provider-specific parameters and requirements.

