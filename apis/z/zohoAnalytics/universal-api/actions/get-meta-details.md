# Zoho Analytics: Get Meta Details

Retrieves workspace or view details from Zoho Analytics.

```
GET https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-meta-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-meta-details?connectionId=$CONNECTION_ID&config=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "config": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-meta-details?${params}`, {
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
| `config` | string | yes | Stringified JSON config that identifies the target workspace or view by name, such as workspaceName, folderName, or viewName. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "workspaces": {
          "orgId": "string",
          "workspaceDesc": "string",
          "workspaceId": "string",
          "workspaceName": "Ava Chen"
        }
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
| `data.workspaces.orgId` | string |  |
| `data.workspaces.workspaceDesc` | string |  |
| `data.workspaces.workspaceId` | string |  |
| `data.workspaces.workspaceName` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `GET /metadetails` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meta-details.md) for the provider-specific parameters and requirements.

