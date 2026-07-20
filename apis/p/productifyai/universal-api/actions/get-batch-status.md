# Productify.ai: Get Batch Status



```
GET https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-batch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productify.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-batch-status?connectionId=$CONNECTION_ID&batchId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productifyai/latest/actions/get-batch-status?${params}`, {
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
| `batchId` | number | yes | Batch identifier returned by a Productify.ai batch creation endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "hasError": true,
      "itemCount": 1,
      "itemProcessedCount": 1,
      "lastUpdatedDate": "2026-05-07T12:00:00.000Z",
      "responseMessage": "string",
      "status": "string",
      "statusMessage": "string",
      "wasSuccessful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | number |  |
| `createdDate` | date |  |
| `hasError` | boolean |  |
| `itemCount` | number |  |
| `itemProcessedCount` | number |  |
| `lastUpdatedDate` | date |  |
| `responseMessage` | string |  |
| `status` | string |  |
| `statusMessage` | string |  |
| `wasSuccessful` | boolean |  |

## Native endpoint

Through the native Productify.ai API, this operation is `GET /Batch/Status` (base URL `https://api.productify.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-status.md) for the provider-specific parameters and requirements.

