# Action1: Get Missing Update

Retrieves available update versions from Action1 for a package.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-missing-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-missing-update?connectionId=$CONNECTION_ID&orgId=string&packageId=package-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "string",
  "packageId": "package-123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-missing-update?${params}`, {
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
| `orgId` | string | yes | Action1 organization ID. |
| `packageId` | string | yes | Missing update package ID. Example: `package-123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "builtin": "string",
      "classification": "string",
      "description": "string",
      "id": "string",
      "internal_notes": "string",
      "kb_number": "string",
      "name": "Ava Chen",
      "optional": "string",
      "organization_ids": "string",
      "platform": "string",
      "reboot_needed": "string",
      "recommended": "string",
      "scope": "string",
      "self": "string",
      "size": "string",
      "status": "string",
      "type": "string",
      "update_type": "string",
      "vendor": "string",
      "versions": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `builtin` | string |  |
| `classification` | string |  |
| `description` | string |  |
| `id` | string |  |
| `internal_notes` | string |  |
| `kb_number` | string |  |
| `name` | string |  |
| `optional` | string |  |
| `organization_ids` | string |  |
| `platform` | string |  |
| `reboot_needed` | string |  |
| `recommended` | string |  |
| `scope` | string |  |
| `self` | string |  |
| `size` | string |  |
| `status` | string |  |
| `type` | string |  |
| `update_type` | string |  |
| `vendor` | string |  |
| `versions` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /updates/:orgId/:packageId` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-missing-update.md) for the provider-specific parameters and requirements.

