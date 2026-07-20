# Abbyy: Process Business Card

Creates a business card OCR task in ABBYY Cloud OCR SDK.

```
POST https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/process-business-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abbyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/process-business-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/process-business-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Business card image or PDF file to process. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Abbyy API returns.

## Native endpoint

Through the native Abbyy API, this operation is `POST /v2/processBusinessCard` (base URL `https://cloud-westus.ocrsdk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-business-card.md) for the provider-specific parameters and requirements.

