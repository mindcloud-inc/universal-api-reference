# Five9: Update User

Updates an existing user in Five9.

```
PUT https://connect.mindcloud.co/v1/universal/five9/latest/actions/update-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Five9 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/five9/latest/actions/update-user-info" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userUID": "string",
  "domainID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/five9/latest/actions/update-user-info', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userUID": "string",
    "domainID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userUID` | string | yes |  |
| `domainID` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Five9 API returns.

## Native endpoint

Through the native Five9 API, this operation is `PATCH https://api.prod.us.five9.net/users/v1/domains/:domainID/users/:userUID` (base URL `https://api.prod.us.five9.net/acl/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-info.md) for the provider-specific parameters and requirements.

