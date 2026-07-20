# Zoho Analytics: List Views

Retrieves views from a Zoho Analytics workspace.

```
GET https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-views?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-views?${params}`, {
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
| `workspaceId` | string | yes | ID of the workspace whose views should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "views": [
          {
            "createdBy": "string",
            "createdTime": "string",
            "folderId": "string",
            "isFavorite": true,
            "lastModifiedBy": "string",
            "lastModifiedTime": "string",
            "parentViewId": "string",
            "sharedBy": "string",
            "viewDesc": "string",
            "viewId": "string",
            "viewName": "Ava Chen",
            "viewType": "string"
          }
        ]
      },
      "status": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.views[].createdBy` | string |  |
| `data.views[].createdTime` | string |  |
| `data.views[].folderId` | string |  |
| `data.views[].isFavorite` | boolean |  |
| `data.views[].lastModifiedBy` | string |  |
| `data.views[].lastModifiedTime` | string |  |
| `data.views[].parentViewId` | string |  |
| `data.views[].sharedBy` | string |  |
| `data.views[].viewDesc` | string |  |
| `data.views[].viewId` | string |  |
| `data.views[].viewName` | string |  |
| `data.views[].viewType` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `GET /workspaces/[:workspace-id]/views` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-views.md) for the provider-specific parameters and requirements.

