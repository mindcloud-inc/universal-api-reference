# Beyond Presence: Get Avatar

Retrieves an avatar from Beyond Presence.

```
GET https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/get-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beyond Presence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/get-avatar?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/get-avatar?${params}`, {
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
| `id` | string | yes | Avatar ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Unique identifier of the avatar. |
| `name` | string | Display name of the avatar. |
| `status` | string | Current avatar status. |
| `visibility` | string | Visibility of the avatar. |

## Native endpoint

Through the native Beyond Presence API, this operation is `GET /v1/avatars/:id` (base URL `https://api.bey.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-avatar.md) for the provider-specific parameters and requirements.

