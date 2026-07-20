# Feathery: Update a Form



```
PUT https://connect.mindcloud.co/v1/universal/feathery/latest/actions/update-a-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/update-a-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feathery/latest/actions/update-a-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form_id` | string | yes | The ID of the form to update. |
| `enabled` | boolean | no | Whether the form should be enabled or disabled. |
| `form_name` | string | no | The new name to set for the form. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `translations` | object | no | A mapping of default text to translations. |
| `integrations[]` | array<object> | no | An array of integrations created in this form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "form_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean | Whether the form is enabled. |
| `form_name` | string | The name of the form. |

## Native endpoint

Through the native Feathery API, this operation is `PATCH /api/form/:form_id/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-form.md) for the provider-specific parameters and requirements.

