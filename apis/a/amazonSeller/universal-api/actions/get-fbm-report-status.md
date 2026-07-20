# Amazon Seller: Get FBM Report Status

Retrieves FBM report details from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-fbm-report-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-fbm-report-status?connectionId=$CONNECTION_ID&reportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-fbm-report-status?${params}`, {
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
| `reportId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "string",
      "dataEndTime": "string",
      "dataStartTime": "string",
      "marketplaceIds": [
        "string"
      ],
      "processingEndTime": "string",
      "processingStartTime": "string",
      "processingStatus": "string",
      "reportDocumentId": "string",
      "reportId": "string",
      "reportType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | string |  |
| `dataEndTime` | string |  |
| `dataStartTime` | string |  |
| `marketplaceIds[]` | string |  |
| `processingEndTime` | string |  |
| `processingStartTime` | string |  |
| `processingStatus` | string |  |
| `reportDocumentId` | string |  |
| `reportId` | string |  |
| `reportType` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET reports/2021-06-30/reports/:reportId` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fbm-report-status.md) for the provider-specific parameters and requirements.

