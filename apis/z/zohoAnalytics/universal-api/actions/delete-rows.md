# Zoho Analytics: Delete Rows

Deletes rows from a Zoho Analytics table.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/delete-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/delete-rows?connectionId=$CONNECTION_ID&workspaceId=string&viewId=string&config=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "viewId": "string",
  "config": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/delete-rows?${params}`, {
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
| `workspaceId` | string | yes | ID of the workspace containing the table view. |
| `viewId` | string | yes | ID of the table view whose rows should be deleted. |
| `config` | string | yes | Stringified JSON payload that defines the rows to delete. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "deletedRows": 1
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
| `data.deletedRows` | number |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `DELETE /workspaces/[:workspace-id]/views/[:view-id]/rows` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-rows.md) for the provider-specific parameters and requirements.

