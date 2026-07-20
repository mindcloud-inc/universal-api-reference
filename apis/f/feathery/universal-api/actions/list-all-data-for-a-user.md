# Feathery: List All Data for a User



```
GET https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-all-data-for-a-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-all-data-for-a-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-all-data-for-a-user?${params}`, {
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
| `id` | string | no | The user ID whose submitted field data you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_text": "string",
      "hidden": true,
      "id": "string",
      "internal_id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | When the field was created. |
| `display_text` | string | The human-friendly field label. |
| `hidden` | boolean | Whether the field is hidden. |
| `id` | string | The field ID. |
| `internal_id` | string | The stable Feathery field identifier. |
| `type` | string | The field type. |
| `updated_at` | date | When the field was last updated. |

## Native endpoint

Through the native Feathery API, this operation is `GET /api/field/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-data-for-a-user.md) for the provider-specific parameters and requirements.

