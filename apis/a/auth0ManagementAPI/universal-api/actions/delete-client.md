# Auth0 Management: Delete Client

Deletes a client from Auth0 Management API.

```
DELETE https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/delete-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auth0 Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/delete-client?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/delete-client?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Auth0 Management API returns.

## Native endpoint

Through the native Auth0 Management API, this operation is `DELETE /clients/{id}` (base URL `https://{{credentials.tenantDomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-client.md) for the provider-specific parameters and requirements.

