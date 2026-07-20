# Zoho Analytics: Update Rows

Updates rows in a Zoho Analytics table.

```
PUT https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/update-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/update-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "viewId": "string",
  "config": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/update-rows', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "viewId": "string",
    "config": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | ID of the workspace containing the table view. |
| `viewId` | string | yes | ID of the table view whose rows should be updated. |
| `config` | string | yes | Stringified JSON payload with criteria plus a columns object containing the updated values. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "invalidColumns": {},
        "updatedColumns": {},
        "updatedRows": 1
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
| `data.invalidColumns` | object |  |
| `data.updatedColumns` | object |  |
| `data.updatedRows` | number |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `PUT /workspaces/[:workspace-id]/views/[:view-id]/rows` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-rows.md) for the provider-specific parameters and requirements.

