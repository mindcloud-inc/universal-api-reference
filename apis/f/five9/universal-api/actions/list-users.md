# Five9: List Users

Retrieves users from Five9.

```
GET https://connect.mindcloud.co/v1/universal/five9/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Five9 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/five9/latest/actions/list-users?connectionId=$CONNECTION_ID&domainID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/five9/latest/actions/list-users?${params}`, {
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
| `email` | string | no |  |
| `lastName` | string | no |  |
| `phoneNumber` | string | no |  |
| `firstName` | string | no |  |
| `domainID` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Five9 API returns.

## Native endpoint

Through the native Five9 API, this operation is `GET https://api.prod.us.five9.net/users/v1/domains/:domainID/users` (base URL `https://api.prod.us.five9.net/acl/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

