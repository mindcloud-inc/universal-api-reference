# AppWright: Search SQL

Retrieves AppWright data with a SQL select query.

```
GET https://connect.mindcloud.co/v1/universal/appWright/latest/actions/search-sql
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AppWright `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appWright/latest/actions/search-sql?connectionId=$CONNECTION_ID&SQL=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "SQL": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appWright/latest/actions/search-sql?${params}`, {
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
| `SQL` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AppWright API returns.

## Native endpoint

Through the native AppWright API, this operation is `POST awAPI/awAPI.asp` (base URL `https://{{credentials.clientId}}.AppWright.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-sql.md) for the provider-specific parameters and requirements.

