# FTrack: Parse Query

Parses a query expression in FTrack.

```
GET https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/parse-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FTrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/parse-query?connectionId=$CONNECTION_ID&expression=select%20id%20from%20Task%20where%20name%20is%20%22Comp%22" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "expression": "select id from Task where name is \"Comp\""
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/parse-query?${params}`, {
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
| `expression` | string | yes | ftrack query expression to parse. Example: `select id from Task where name is "Comp"`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FTrack API returns.

## Native endpoint

Through the native FTrack API, this operation is `POST /api` (base URL `{{credentials.serverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-query.md) for the provider-specific parameters and requirements.

