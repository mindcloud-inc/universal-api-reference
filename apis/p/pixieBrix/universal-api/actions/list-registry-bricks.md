# PixieBrix: List Registry Bricks

Retrieves brick packages from the PixieBrix registry.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-registry-bricks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-registry-bricks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-registry-bricks?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `kind` | string | no | Registry brick kind filter. |
| `kindIn` | string | no | Comma-separated registry brick kinds to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "definitions": {},
      "extensionPoints": [
        {}
      ],
      "inputSchema": {},
      "kind": "string",
      "metadata": {},
      "options": {},
      "pipeline": [
        {}
      ],
      "sharing": {},
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `definitions` | object |  |
| `extensionPoints` | array<object> |  |
| `inputSchema` | object |  |
| `kind` | string |  |
| `metadata` | object |  |
| `options` | object |  |
| `pipeline` | array<object> |  |
| `sharing` | object |  |
| `updated_at` | date |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/registry/bricks/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-registry-bricks.md) for the provider-specific parameters and requirements.

