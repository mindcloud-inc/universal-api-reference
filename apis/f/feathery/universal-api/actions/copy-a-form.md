# Feathery: Copy a Form



```
POST https://connect.mindcloud.co/v1/universal/feathery/latest/actions/copy-a-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/copy-a-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form_name": "Ava Chen",
  "copy_form_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feathery/latest/actions/copy-a-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form_name": "Ava Chen",
    "copy_form_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form_name` | string | yes | The name of the new copied form. |
| `copy_form_id` | string | yes | The ID of the form to copy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "internal_id": "string",
      "name": "Ava Chen",
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the copied form is active. |
| `created_at` | date | When the form was created. |
| `id` | string | The form ID. |
| `internal_id` | string | The internal Feathery form identifier. |
| `name` | string | The form name. |
| `tags` | array<string> | The tags on the copied form. |
| `updated_at` | date | When the form was last updated. |

## Native endpoint

Through the native Feathery API, this operation is `POST /api/form/copy/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-a-form.md) for the provider-specific parameters and requirements.

