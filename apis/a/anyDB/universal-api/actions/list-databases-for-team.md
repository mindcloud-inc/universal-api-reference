# AnyDB: List Databases For Team

Retrieves databases for a team in AnyDB.

```
GET https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/list-databases-for-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnyDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/list-databases-for-team?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/list-databases-for-team?${params}`, {
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
| `teamId` | string | yes | The AnyDB team ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AnyDB API returns.

## Native endpoint

Through the native AnyDB API, this operation is `GET /api/integrations/ext/listdbsforteam` (base URL `https://app.anydb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-databases-for-team.md) for the provider-specific parameters and requirements.

