# Mixpanel: Query Segmentation Report

Retrieves a segmentation report from Mixpanel.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-segmentation-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-segmentation-report?connectionId=$CONNECTION_ID&event=Signed%20Up&fromDate=2026-03-01&toDate=2026-03-12" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event": "Signed Up",
  "fromDate": "2026-03-01",
  "toDate": "2026-03-12"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-segmentation-report?${params}`, {
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
| `event` | string | yes | Single event name to analyze. Example: `Signed Up`. |
| `fromDate` | string | yes | Inclusive start date in YYYY-MM-DD format. Example: `2026-03-01`. |
| `toDate` | string | yes | Inclusive end date in YYYY-MM-DD format. Example: `2026-03-12`. |
| `on` | string | no | Property expression used to segment the event. Example: `properties["Plan"]`. |
| `unit` | string | no | Time bucket unit. Example: `day`. |
| `interval` | number | no | Optional bucket interval. Example: `7`. |
| `where` | string | no | Expression used to filter events. Example: `properties["Browser"] == "Chrome"`. |
| `limit` | number | no | Maximum number of segmentation values to return when using `on`. Example: `25`. |
| `type` | string | no | Aggregation type: general, unique, or average. Example: `general`. |
| `format` | string | no | Optional response format. Example: `json`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | no | Required when authenticating with a Mixpanel service account. Example: `12345`. |
| `workspaceId` | number | no | Optional Mixpanel workspace ID. Example: `98765`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "series": [
          "string"
        ]
      },
      "legendSize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.series[]` | string | Date buckets returned for the segmentation report. |
| `legendSize` | number | Number of legend entries in the report. |

## Native endpoint

Through the native Mixpanel API, this operation is `GET /query/segmentation` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-segmentation-report.md) for the provider-specific parameters and requirements.

