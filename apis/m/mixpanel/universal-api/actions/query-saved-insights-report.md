# Mixpanel: Query Saved Insights Report

Retrieves a saved insights report from Mixpanel.

```
GET https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-saved-insights-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-saved-insights-report?connectionId=$CONNECTION_ID&bookmarkId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookmarkId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/query-saved-insights-report?${params}`, {
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
| `bookmarkId` | number | yes | Saved Insights report ID from the Mixpanel URL. Example: `12345`. |

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
      "computedAt": "string",
      "dateRange": {
        "fromDate": "string",
        "toDate": "string"
      },
      "headers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `computedAt` | string | Timestamp when Mixpanel computed the report. |
| `dateRange.fromDate` | string | Report start date. |
| `dateRange.toDate` | string | Report end date. |
| `headers[]` | string | Series labels returned by Mixpanel. |

## Native endpoint

Through the native Mixpanel API, this operation is `GET /query/insights` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-saved-insights-report.md) for the provider-specific parameters and requirements.

