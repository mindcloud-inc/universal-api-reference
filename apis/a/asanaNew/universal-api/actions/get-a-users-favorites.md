# Asana: Get a user's favorites

Retrieves a user's favorites from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-users-favorites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-users-favorites?connectionId=$CONNECTION_ID&limit=25&offset=0&userGid=string&resourceType=string&workspace=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userGid": "string",
  "resourceType": "string",
  "workspace": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-a-users-favorites?${params}`, {
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
| `userGid` | string | yes |  |
| `resourceType` | string | yes |  |
| `workspace` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `optPretty` | boolean | no |  |
| `optFields` | list<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `GET users/:user_gid/favorites` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-a-users-favorites.md) for the provider-specific parameters and requirements.

