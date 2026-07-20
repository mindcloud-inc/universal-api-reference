# Zoho Analytics: Get View

Retrieves a view from Zoho Analytics by ID.

```
GET https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-view?connectionId=$CONNECTION_ID&viewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-view?${params}`, {
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
| `viewId` | string | yes | ID of the view to inspect. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `config` | string | no | Optional JSON configuration string such as {"withInvolvedMetaInfo":true}. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "views": {
          "createdBy": "string",
          "createdByName": "Ava Chen",
          "createdByZuId": "string",
          "createdTime": "string",
          "lastDesignModifiedBy": "string",
          "lastDesignModifiedByName": "Ava Chen",
          "lastDesignModifiedByZuId": "string",
          "lastDesignModifiedTime": "string",
          "orgId": "string",
          "viewDesc": "string",
          "viewId": "string",
          "viewName": "Ava Chen",
          "viewType": "string",
          "workspaceId": "string"
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
| `data.views.createdBy` | string |  |
| `data.views.createdByName` | string |  |
| `data.views.createdByZuId` | string |  |
| `data.views.createdTime` | string |  |
| `data.views.lastDesignModifiedBy` | string |  |
| `data.views.lastDesignModifiedByName` | string |  |
| `data.views.lastDesignModifiedByZuId` | string |  |
| `data.views.lastDesignModifiedTime` | string |  |
| `data.views.orgId` | string |  |
| `data.views.viewDesc` | string |  |
| `data.views.viewId` | string |  |
| `data.views.viewName` | string |  |
| `data.views.viewType` | string |  |
| `data.views.workspaceId` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `GET /views/[:view-id]` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-view.md) for the provider-specific parameters and requirements.

