# LoginRadius: List User Profiles

Retrieves user profiles from LoginRadius by page.

```
GET https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/list-user-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/list-user-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/list-user-profiles?${params}`, {
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
| `next` | string | no | Pagination token returned by the previous page. Example: `eyJvZmZzZXQiOjEwMH0=`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `region` | string | no | Region filter for the results. Example: `us`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LoginRadius API returns.

## Native endpoint

Through the native LoginRadius API, this operation is `GET https://cloud-api.loginradius.com/identity` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-profiles.md) for the provider-specific parameters and requirements.

