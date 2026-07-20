# Postmaster+: Delete Single Email

Deletes single email intelligence from Postmaster+.

```
DELETE https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/delete-single-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/delete-single-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/delete-single-email?${params}`, {
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
| `email` | string | yes | The email address to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the email was deleted. |
| `message` | string | Delete confirmation message. |

## Native endpoint

Through the native Postmaster+ API, this operation is `DELETE /api/v1/intelligence/single-emails/:email` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-single-email.md) for the provider-specific parameters and requirements.

