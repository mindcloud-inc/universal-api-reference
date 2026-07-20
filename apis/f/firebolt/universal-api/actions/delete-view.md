# Firebolt: Delete View

Deletes an existing view from Firebolt.

```
DELETE https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/delete-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/delete-view?connectionId=$CONNECTION_ID&engineHost=account-1-mindcloud.api.us-east-1.app.firebolt.io&viewName=mc_fb_delete_view_20260422" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
  "viewName": "mc_fb_delete_view_20260422"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/delete-view?${params}`, {
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
| `engineHost` | string | yes | User engine host to execute the DROP VIEW statement against. Example: `account-1-mindcloud.api.us-east-1.app.firebolt.io`. |
| `viewName` | string | yes | The Firebolt view to delete. Example: `mc_fb_delete_view_20260422`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineName` | string | no | Optional engine name to send as the Firebolt engine query parameter. Example: `mc_fb_act_20260422_engine`. |
| `database` | string | no | Optional Firebolt database to execute the DROP VIEW statement in. Example: `mc_fb_act_20260422_db`. |
| `ifExists` | boolean | no | When true, suppresses the error if the view does not exist. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "meta": [
        {}
      ],
      "query": {},
      "rows": 1,
      "statistics": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned data rows. |
| `meta` | array<object> | Column metadata for the response. |
| `query` | object | Firebolt query metadata. |
| `rows` | number | Number of rows returned in the data payload. |
| `statistics` | object | Firebolt execution statistics. |

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineHost` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-view.md) for the provider-specific parameters and requirements.

