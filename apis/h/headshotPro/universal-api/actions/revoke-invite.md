# HeadshotPro: Revoke Invite

Revokes an invite in HeadshotPro by email address.

```
DELETE https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/revoke-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeadshotPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/revoke-invite?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/revoke-invite?${params}`, {
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
| `email` | string | yes | Email address of the invite to revoke. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `input` | object | Echoed invite input. |
| `message` | string | Invite revocation result message. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native HeadshotPro API, this operation is `POST /organization/invites/revoke` (base URL `https://server.headshotpro.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-invite.md) for the provider-specific parameters and requirements.

