# Zoho Analytics: List Folders

Retrieves folders from a Zoho Analytics workspace.

```
GET https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-folders?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-folders?${params}`, {
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
| `workspaceId` | string | yes | ID of the workspace whose folders should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "folders": [
          {
            "folderDesc": "string",
            "folderId": "string",
            "folderIndex": 1,
            "folderName": "Ava Chen",
            "isDefault": true,
            "parentFolderId": "string"
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
| `data.folders[].folderDesc` | string |  |
| `data.folders[].folderId` | string |  |
| `data.folders[].folderIndex` | number |  |
| `data.folders[].folderName` | string |  |
| `data.folders[].isDefault` | boolean |  |
| `data.folders[].parentFolderId` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `GET /workspaces/[:workspace-id]/folders` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

