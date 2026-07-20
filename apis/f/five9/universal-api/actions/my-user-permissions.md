# Five9: My User Permission's

Retrieves your user permissions from Five9.

```
GET https://connect.mindcloud.co/v1/universal/five9/latest/actions/my-user-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Five9 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/five9/latest/actions/my-user-permissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/five9/latest/actions/my-user-permissions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Five9 API returns.

## Native endpoint

Through the native Five9 API, this operation is `GET https://api.prod.us.five9.net/acl/v1/domains/130744/my-ui-permissions` (base URL `https://api.prod.us.five9.net/acl/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/my-user-permissions.md) for the provider-specific parameters and requirements.

