# Firebolt: Create View

Creates a new view in Firebolt.

```
POST https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/create-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/create-view" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineUrl": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
  "engineName": "mc_fb_act_20260422_engine",
  "database": "mc_fb_act_20260422_db",
  "viewName": "mc_stage3_20260422_view2",
  "selectStatement": "SELECT 1 AS value"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/create-view', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineUrl": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
    "engineName": "mc_fb_act_20260422_engine",
    "database": "mc_fb_act_20260422_db",
    "viewName": "mc_stage3_20260422_view2",
    "selectStatement": "SELECT 1 AS value"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineUrl` | string | yes | Firebolt user engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. Example: `account-1-mindcloud.api.us-east-1.app.firebolt.io`. |
| `engineName` | string | yes | Name of the user engine, for example mc_fb_act_20260422_engine. Example: `mc_fb_act_20260422_engine`. |
| `database` | string | yes | Database to use for the statement. Example: `mc_fb_act_20260422_db`. |
| `viewName` | string | yes | Name of the view to create. Example: `mc_stage3_20260422_view2`. |
| `selectStatement` | string | yes | SELECT statement that defines the view. Example: `SELECT 1 AS value`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Firebolt API returns.

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineUrl` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-view.md) for the provider-specific parameters and requirements.

