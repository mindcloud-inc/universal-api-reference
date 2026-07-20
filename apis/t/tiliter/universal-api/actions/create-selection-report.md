# Tiliter: Create Selection Report

Creates a selection report in the Tiliter Recognition API.

```
POST https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-selection-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-selection-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recognitionId": "string",
  "selectionMethod": "string",
  "selectedProductId": "string",
  "saleInfo": {},
  "selectionTime": "2026-05-07T12:00:00.000Z",
  "transactionId": "string",
  "lineItemId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-selection-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recognitionId": "string",
    "selectionMethod": "string",
    "selectedProductId": "string",
    "saleInfo": {},
    "selectionTime": "2026-05-07T12:00:00.000Z",
    "transactionId": "string",
    "lineItemId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recognitionId` | string | yes |  |
| `selectionMethod` | string | yes |  |
| `selectedProductId` | string | yes |  |
| `saleInfo` | object | yes |  |
| `selectionTime` | date | yes |  |
| `transactionId` | string | yes |  |
| `lineItemId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lossDetection": {
        "status": "string"
      },
      "recognitionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lossDetection` | object |  |
| `lossDetection.status` | string |  |
| `recognitionId` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `POST /recognition/:recognition_id/selection_report` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-selection-report.md) for the provider-specific parameters and requirements.

