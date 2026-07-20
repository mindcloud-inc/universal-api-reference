# Zoho Analytics: Delete View

Deletes a view from Zoho Analytics.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/delete-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/delete-view?connectionId=$CONNECTION_ID&workspaceId=string&viewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "viewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/delete-view?${params}`, {
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
| `workspaceId` | string | yes | ID of the workspace containing the view. |
| `viewId` | string | yes | ID of the view to move to trash. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `config` | string | no | Optional stringified JSON delete configuration. Leave this empty for a standard delete request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Analytics API returns.

## Native endpoint

Through the native Zoho Analytics API, this operation is `DELETE /workspaces/[:workspace-id]/views/[:view-id]` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-view.md) for the provider-specific parameters and requirements.

