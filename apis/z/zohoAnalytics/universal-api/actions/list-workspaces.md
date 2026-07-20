# Zoho Analytics: List Workspaces

Retrieves accessible workspaces from Zoho Analytics.

```
GET https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-workspaces?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "ownedWorkspaces": [
          {
            "createdBy": "string",
            "createdTime": "string",
            "isDefault": true,
            "orgId": "string",
            "workspaceDesc": "string",
            "workspaceId": "string",
            "workspaceName": "Ava Chen"
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
| `data.ownedWorkspaces[].createdBy` | string |  |
| `data.ownedWorkspaces[].createdTime` | string |  |
| `data.ownedWorkspaces[].isDefault` | boolean |  |
| `data.ownedWorkspaces[].orgId` | string |  |
| `data.ownedWorkspaces[].workspaceDesc` | string |  |
| `data.ownedWorkspaces[].workspaceId` | string |  |
| `data.ownedWorkspaces[].workspaceName` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `GET /workspaces` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

