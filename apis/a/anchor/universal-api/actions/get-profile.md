# Anchor: Get Profile

Retrieves a profile from Anchor.

```
GET https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anchor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-profile?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anchor/latest/actions/get-profile?${params}`, {
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
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "description": "string",
      "name": "Ava Chen",
      "session_id": "string",
      "source": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `description` | string |  |
| `name` | string |  |
| `session_id` | string |  |
| `source` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Anchor API, this operation is `GET /v1/profiles/:name` (base URL `https://api.anchorbrowser.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.

