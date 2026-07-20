# Firebolt: Firebolt Query Helper

Retrieves query results from Firebolt.

```
GET https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/firebolt-query-helper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/firebolt-query-helper?connectionId=$CONNECTION_ID&engineHost=string&engineName=Ava%20Chen&database=string&sqlQuery=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "engineHost": "string",
  "engineName": "Ava Chen",
  "database": "string",
  "sqlQuery": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/firebolt-query-helper?${params}`, {
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
| `engineHost` | string | yes | Firebolt engine host without protocol. |
| `engineName` | string | yes | User engine name for the user-engine URL. |
| `database` | string | yes | Firebolt database name for the user-engine URL. |
| `sqlQuery` | string | yes | Raw SQL statement to execute. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Firebolt API returns.

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineHost?engine=:engineName&database=:database&output_format=JSON_Compact` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/firebolt-query-helper.md) for the provider-specific parameters and requirements.

