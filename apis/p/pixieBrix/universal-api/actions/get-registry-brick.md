# PixieBrix: Get Registry Brick

Retrieves a brick package from the PixieBrix registry.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-registry-brick
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-registry-brick?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-registry-brick?${params}`, {
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
| `name` | string | yes | PixieBrix registry package name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `kind` | string | no | Registry brick kind filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "sharing": {},
      "updated_at": "2026-05-07T12:00:00.000Z",
      "verbose_name": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `sharing` | object |  |
| `updated_at` | date |  |
| `verbose_name` | string |  |
| `version` | string |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/registry/bricks/:name/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-registry-brick.md) for the provider-specific parameters and requirements.

