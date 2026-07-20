# Feathery: Create a Form



```
POST https://connect.mindcloud.co/v1/universal/feathery/latest/actions/create-a-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/create-a-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form_name": "Ava Chen",
  "template_form_id": "string",
  "steps[]": [
    {}
  ],
  "navigation_rules[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feathery/latest/actions/create-a-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form_name": "Ava Chen",
    "template_form_id": "string",
    "steps[]": [{}],
    "navigation_rules[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form_name` | string | yes | The unique name of the new form. |
| `template_form_id` | string | yes | The ID of the template form to copy from. |
| `steps[]` | array<object> | yes | An array of steps to create in the new form. |
| `navigation_rules[]` | array<object> | yes | An array of navigation rules connecting the steps. |
| `enabled` | boolean | no | Whether the created form should be enabled. If omitted, it inherits the template form status. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logic_rules[]` | array<object> | no | An array of advanced logic rules to associate with the form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "internal_id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The form ID. |
| `internal_id` | string | The internal Feathery form identifier. |
| `name` | string | The form name. |

## Native endpoint

Through the native Feathery API, this operation is `POST /api/form/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-form.md) for the provider-specific parameters and requirements.

