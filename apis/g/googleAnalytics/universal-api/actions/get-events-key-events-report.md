# Google Analytics: Get Events and Key Events Report



```
GET https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/get-events-key-events-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/get-events-key-events-report?connectionId=$CONNECTION_ID&propertyId=123456789&dateRanges%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "123456789",
  "dateRanges[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/get-events-key-events-report?${params}`, {
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
| `propertyId` | string | yes | GA4 property ID without the properties/ prefix Example: `123456789`. |
| `dateRanges[]` | array<object> | yes | GA4 date ranges, such as 30daysAgo through today Default: `[{"endDate":"today","startDate":"30daysAgo"}]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum report rows to return Default: `1000`. |
| `offset` | number | no | Zero-based row offset Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dimensionHeaders": [
        {}
      ],
      "kind": "string",
      "metadata": {},
      "metricHeaders": [
        {}
      ],
      "rowCount": 1,
      "rows": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dimensionHeaders` | array<object> | Requested dimension columns in response order |
| `kind` | string | Google Analytics response type |
| `metadata` | object | Property currency and timezone metadata |
| `metricHeaders` | array<object> | Requested metric columns in response order |
| `rowCount` | number | Total number of rows matching the report |
| `rows` | array<object> | Report rows containing dimensionValues and metricValues |

## Native endpoint

Through the native Google Analytics API, this operation is `POST https://analyticsdata.googleapis.com/v1beta/properties/:propertyId:urlEnd` (base URL `https://analyticsdata.googleapis.com/v1beta`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-events-key-events-report.md) for the provider-specific parameters and requirements.

