# Mixpanel: Query Retention Report

Retrieves a retention report from Mixpanel.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-retention-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-retention-report?connectionId=$CONNECTION_ID&fromDate=2026-03-01&toDate=2026-03-12" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "2026-03-01",
  "toDate": "2026-03-12"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-retention-report?${params}`, {
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
| `fromDate` | string | yes | Inclusive start date in YYYY-MM-DD format. Example: `2026-03-01`. |
| `toDate` | string | yes | Inclusive end date in YYYY-MM-DD format. Example: `2026-03-12`. |
| `retentionType` | string | no | Retention mode: birth or compounded. Example: `birth`. |
| `bornEvent` | string | no | First event for birth-retention cohorts. Example: `Signed Up`. |
| `event` | string | no | Event to count as returning activity. Example: `Logged In`. |
| `bornWhere` | string | no | Filter expression for the born event. Example: `properties["Plan"] == "Pro"`. |
| `where` | string | no | Filter expression for returning events. Example: `properties["Browser"] == "Chrome"`. |
| `interval` | number | no | Bucket size for retention intervals. Example: `1`. |
| `intervalCount` | number | no | Number of intervals to return. Example: `4`. |
| `unit` | string | no | Interval unit: day, week, or month. Example: `day`. |
| `unboundedRetention` | boolean | no | Accumulate retention counts from right to left when true. Example: `true`. |
| `on` | string | no | Property expression used to segment returning events. Example: `properties["Plan"]`. |
| `limit` | number | no | Maximum number of segmentation values to return when using `on`. Example: `25`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | no | Required when authenticating with a Mixpanel service account. Example: `12345`. |
| `workspaceId` | number | no | Optional Mixpanel workspace ID. Example: `98765`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mixpanel API returns.

## Native endpoint

Through the native Mixpanel API, this operation is `GET /query/retention` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-retention-report.md) for the provider-specific parameters and requirements.

