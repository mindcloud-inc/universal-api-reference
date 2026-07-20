# Doctly: Update Extractor



```
PUT https://connect.mindcloud.co/v1/universal/doctly/latest/actions/update-extractor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doctly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/doctly/latest/actions/update-extractor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "extractorId": "987fcdeb-a654-3210-9876-543210987654"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/doctly/latest/actions/update-extractor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "extractorId": "987fcdeb-a654-3210-9876-543210987654"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extractorId` | string | yes | Unique extractor UUID to update. Example: `987fcdeb-a654-3210-9876-543210987654`. |
| `name` | string | no | New display name for the extractor. Example: `Invoice Parser v2`. |
| `slug` | string | no | New unique URL-friendly slug for the extractor. Example: `invoice-parser-v2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Doctly API returns.

## Native endpoint

Through the native Doctly API, this operation is `PUT /e/:extractorId` (base URL `https://api.doctly.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-extractor.md) for the provider-specific parameters and requirements.

