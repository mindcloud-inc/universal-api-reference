# Zoho Analytics: Create Workspace

Creates a workspace in Zoho Analytics.

```
POST https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/create-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/create-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "config": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/create-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "config": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `config` | string | yes | Required stringified JSON workspace configuration such as workspaceName. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "workspaceId": "string"
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
| `data.workspaceId` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `POST /workspaces` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace.md) for the provider-specific parameters and requirements.

