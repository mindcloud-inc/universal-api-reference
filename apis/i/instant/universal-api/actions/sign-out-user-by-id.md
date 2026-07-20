# Instant: Sign Out User by ID

Signs out an Instant user by ID.

```
DELETE https://connect.mindcloud.co/v1/universal/instant/latest/actions/sign-out-user-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instant/latest/actions/sign-out-user-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instant/latest/actions/sign-out-user-by-id?${params}`, {
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
| `id` | string | yes | Instant user ID whose sessions should be revoked. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean | Whether the sign-out request succeeded. |

## Native endpoint

Through the native Instant API, this operation is `POST /admin/sign_out` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sign-out-user-by-id.md) for the provider-specific parameters and requirements.

