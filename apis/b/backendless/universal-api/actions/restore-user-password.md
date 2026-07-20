# Backendless: Restore User Password

Starts password recovery for a Backendless user.

```
GET https://connect.mindcloud.co/v1/universal/backendless/latest/actions/restore-user-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Backendless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/backendless/latest/actions/restore-user-password?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/backendless/latest/actions/restore-user-password?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Backendless API returns.

## Native endpoint

Through the native Backendless API, this operation is `GET /{{credentials.applicationId}}/{{credentials.apiKey}}/users/restorepassword/{identity}` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-user-password.md) for the provider-specific parameters and requirements.

