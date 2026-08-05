# Google Analytics: Run Funnel Report



```
GET https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/run-funnel-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/run-funnel-report?connectionId=$CONNECTION_ID&propertyId=123456789&dateRanges%5B%5D=%5Bobject%20Object%5D&funnel=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "123456789",
  "dateRanges[]": "[object Object]",
  "funnel": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/run-funnel-report?${params}`, {
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
| `dateRanges[]` | array<object> | yes | Default: `[{"endDate":"today","startDate":"30daysAgo"}]`. |
| `funnel` | object | yes | Early-preview GA4 funnel definition containing ordered funnel steps |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Default: `1000`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Analytics API returns.

## Native endpoint

Through the native Google Analytics API, this operation is `POST https://analyticsdata.googleapis.com/v1alpha/properties/:propertyId:urlEnd` (base URL `https://analyticsdata.googleapis.com/v1beta`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-funnel-report.md) for the provider-specific parameters and requirements.

