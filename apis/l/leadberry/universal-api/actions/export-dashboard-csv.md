# Leadberry: Export Dashboard CSV



```
GET https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/export-dashboard-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadberry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/export-dashboard-csv?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/export-dashboard-csv?${params}`, {
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
| `allResults` | string | no | Dashboard results payload to export. |
| `companyAndSocialData` | string | no | Whether to include company and social data in the export. |
| `emailAddresses` | string | no | Whether to include email addresses in the export. |
| `extraData.aid` | string | no | Leadberry account ID for the exported dashboard view. |
| `extraData.exportFrom` | string | no | Export start date. |
| `extraData.exportTo` | string | no | Export end date. |
| `extraData.pid` | string | no | Leadberry profile ID for the exported dashboard view. |
| `extraData.profileName` | string | no | Profile name for the exported dashboard view. |
| `extraData.websiteUrl` | string | no | Website URL for the exported dashboard view. |
| `extraData.wid` | string | no | Leadberry website ID for the exported dashboard view. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadberry API returns.

## Native endpoint

Through the native Leadberry API, this operation is `POST /data/downloadCSVFromDashboard` (base URL `https://app.leadberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-dashboard-csv.md) for the provider-specific parameters and requirements.

