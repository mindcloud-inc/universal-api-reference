# Zoho Analytics: Create Query Table

Creates a query table in Zoho Analytics.

```
POST https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/create-query-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/create-query-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "config": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/create-query-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "config": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | ID of the workspace where the query table should be created. |
| `config` | string | yes | Required stringified JSON query-table definition including the SQL query. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "viewId": "string"
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
| `data.viewId` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `POST /workspaces/[:workspace-id]/querytables` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-query-table.md) for the provider-specific parameters and requirements.

