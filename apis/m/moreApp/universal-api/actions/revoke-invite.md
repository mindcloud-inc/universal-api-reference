# MoreApp: Revoke Invite

Revokes an invite in MoreApp.

```
DELETE https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/revoke-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/revoke-invite?connectionId=$CONNECTION_ID&customerId=209321&id=69bc4758994b3bfa30c0bbd3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "209321",
  "id": "69bc4758994b3bfa30c0bbd3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/revoke-invite?${params}`, {
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
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `id` | string | yes | MoreApp invite identifier. Default: `69bc4758994b3bfa30c0bbd3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Empty response body on successful invite revocation; presence indicates the request completed. |

## Native endpoint

Through the native MoreApp API, this operation is `DELETE /api/v2/customers/{{customerId}}/invites/{{id}}` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-invite.md) for the provider-specific parameters and requirements.

