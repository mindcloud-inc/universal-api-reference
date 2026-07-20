# Sign: Get invite

Retrieves a dossier invite from CM.com Sign.

```
GET https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-invite?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sign/latest/actions/get-invite?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sign API returns.

## Native endpoint

Through the native Sign API, this operation is `GET /dossiers/{dossierId}/invites/{inviteId}` (base URL `https://api.cm.com/sign-sandbox/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invite.md) for the provider-specific parameters and requirements.

