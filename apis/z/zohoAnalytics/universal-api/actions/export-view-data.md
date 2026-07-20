# Zoho Analytics: Export View Data

Exports view data from Zoho Analytics.

```
GET https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/export-view-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/export-view-data?connectionId=$CONNECTION_ID&workspaceId=string&viewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "viewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/export-view-data?${params}`, {
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
| `workspaceId` | string | yes | ID of the workspace containing the view to export. |
| `viewId` | string | yes | ID of the view to export. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `config` | string | no | Optional stringified JSON export configuration such as responseFormat or criteria. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Analytics API returns.

## Native endpoint

Through the native Zoho Analytics API, this operation is `GET /workspaces/[:workspace-id]/views/[:view-id]/data` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-view-data.md) for the provider-specific parameters and requirements.

