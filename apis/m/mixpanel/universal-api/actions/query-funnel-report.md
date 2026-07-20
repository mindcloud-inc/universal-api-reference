# Mixpanel: Query Funnel Report

Retrieves a funnel report from Mixpanel.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-funnel-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-funnel-report?connectionId=$CONNECTION_ID&funnelId=24680&fromDate=2026-03-01&toDate=2026-03-12" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "funnelId": "24680",
  "fromDate": "2026-03-01",
  "toDate": "2026-03-12"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-funnel-report?${params}`, {
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
| `funnelId` | number | yes | Saved funnel ID from Mixpanel. Example: `24680`. |
| `fromDate` | string | yes | Inclusive start date in YYYY-MM-DD format. Example: `2026-03-01`. |
| `toDate` | string | yes | Inclusive end date in YYYY-MM-DD format. Example: `2026-03-12`. |
| `length` | number | no | Optional funnel completion window length. Example: `30`. |
| `lengthUnit` | string | no | Unit for the funnel completion window length. Example: `day`. |
| `interval` | number | no | Optional bucket size in days. Example: `7`. |
| `unit` | string | no | Bucket unit: day, week, or month. Example: `day`. |
| `on` | string | no | Property expression to segment the funnel on. Example: `properties["Plan"]`. |
| `where` | string | no | Expression used to filter funnel events. Example: `properties["Browser"] == "Chrome"`. |
| `limit` | number | no | Maximum number of segmentation values to return when using `on`. Example: `25`. |

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
      "meta": {
        "dates": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.dates[]` | string | Date buckets returned for the funnel report. |

## Native endpoint

Through the native Mixpanel API, this operation is `GET /query/funnels` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-funnel-report.md) for the provider-specific parameters and requirements.

