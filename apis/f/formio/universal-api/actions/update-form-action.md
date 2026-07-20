# Form.io: Update Form Action

Updates an existing form action in your Form.io project.

```
PUT https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-form-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-form-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "actionId": "string",
  "title": "string",
  "name": "Ava Chen",
  "handler[]": [
    "string"
  ],
  "method[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formio/latest/actions/update-form-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "actionId": "string",
    "title": "string",
    "name": "Ava Chen",
    "handler[]": ["string"],
    "method[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The form ID that owns the action. |
| `actionId` | string | yes | The form action ID. |
| `title` | string | yes | The action title. |
| `name` | string | yes | The action type name, such as save or role. |
| `handler[]` | array<string> | yes | One or more handler stages for the action. |
| `method[]` | array<string> | yes | One or more submission methods that trigger the action. |
| `priority` | number | no | The action priority. |
| `settings` | object | no | Action settings object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "form": "string",
      "handler": [
        "string"
      ],
      "machineName": "Ava Chen",
      "method": [
        "string"
      ],
      "name": "Ava Chen",
      "priority": 1,
      "settings": {},
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `form` | string |  |
| `handler` | array<string> |  |
| `machineName` | string |  |
| `method` | array<string> |  |
| `name` | string |  |
| `priority` | number |  |
| `settings` | object |  |
| `title` | string |  |

## Native endpoint

Through the native Form.io API, this operation is `PUT /form/:formId/action/:actionId` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-action.md) for the provider-specific parameters and requirements.

