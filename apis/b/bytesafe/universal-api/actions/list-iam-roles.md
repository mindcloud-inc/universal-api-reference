# Bytesafe: List IAM Roles

Retrieves role-based access control roles from Bytesafe.

```
GET https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/list-iam-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bytesafe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/list-iam-roles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/list-iam-roles?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bytesafe API returns.

## Native endpoint

Through the native Bytesafe API, this operation is `GET /iam/roles` (base URL `https://mindcloud.bytesafe.dev/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-iam-roles.md) for the provider-specific parameters and requirements.

