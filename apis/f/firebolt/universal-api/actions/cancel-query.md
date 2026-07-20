# Firebolt: Cancel Query

Deletes a running query from Firebolt.

```
DELETE https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/cancel-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/cancel-query?connectionId=$CONNECTION_ID&engineUrl=account-1-mindcloud.api.us-east-1.app.firebolt.io&queryId=c1ecdc7f-2acb-4c3f-8f44-08a6200e718c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "engineUrl": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
  "queryId": "c1ecdc7f-2acb-4c3f-8f44-08a6200e718c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/cancel-query?${params}`, {
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
| `engineUrl` | string | yes | Firebolt engine URL host used to cancel the query. Example: `account-1-mindcloud.api.us-east-1.app.firebolt.io`. |
| `queryId` | string | yes | Firebolt query id to cancel. Example: `c1ecdc7f-2acb-4c3f-8f44-08a6200e718c`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineName` | string | no | User engine name used to run the cancel command. Example: `mc_fb_act_20260422_engine`. |
| `database` | string | no | Database to target for user-engine cancel commands when required. Example: `mc_fb_act_20260422_db`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Firebolt API returns.

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineUrl` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-query.md) for the provider-specific parameters and requirements.

