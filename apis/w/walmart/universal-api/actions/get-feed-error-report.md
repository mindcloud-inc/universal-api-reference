# Walmart: Get Feed Error Report

Download a detailed error report for a submitted feed.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-feed-error-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-feed-error-report?connectionId=$CONNECTION_ID&feedType=False&feedId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedType": "False",
  "feedId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-feed-error-report?${params}`, {
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
| `feedType` | list<string> | yes | When true, includes detailed ingestion records for each item in the feed. Example: `False`. |
| `feedId` | string | yes | A unique ID returned from the Bulk Upload API, used for tracking the feed file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelType": "string",
      "createdBy": "string",
      "feedId": "string",
      "feedStatus": "string",
      "feedSubmissionDate": "2026-05-07T12:00:00.000Z",
      "itemDetails": {
        "itemIngestionStatus": [
          {
            "index": 1,
            "ingestionStatus": "string",
            "itemid": "string",
            "martId": 1,
            "sku": "string"
          }
        ]
      },
      "itemsFailed": 1,
      "itemsProcessing": 1,
      "itemsReceived": 1,
      "itemsSucceeded": 1,
      "limit": 1,
      "offset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelType` | string |  |
| `createdBy` | string |  |
| `feedId` | string |  |
| `feedStatus` | string |  |
| `feedSubmissionDate` | date |  |
| `itemDetails.itemIngestionStatus[].index` | number |  |
| `itemDetails.itemIngestionStatus[].ingestionStatus` | string |  |
| `itemDetails.itemIngestionStatus[].itemid` | string |  |
| `itemDetails.itemIngestionStatus[].martId` | number |  |
| `itemDetails.itemIngestionStatus[].sku` | string |  |
| `itemsFailed` | number |  |
| `itemsProcessing` | number |  |
| `itemsReceived` | number |  |
| `itemsSucceeded` | number |  |
| `limit` | number |  |
| `offset` | number |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/feeds/:feedId/errorReport` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed-error-report.md) for the provider-specific parameters and requirements.

