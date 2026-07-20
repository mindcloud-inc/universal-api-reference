# PixieBrix: Get Package

Retrieves a package from PixieBrix.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-package?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/get-package?${params}`, {
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
| `id` | string | yes | PixieBrix package UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `sharing` | object |  |
| `updated_at` | date |  |
| `verbose_name` | string |  |
| `version` | string |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/bricks/:id/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package.md) for the provider-specific parameters and requirements.

