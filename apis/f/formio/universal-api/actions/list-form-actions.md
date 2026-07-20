# Form.io: List Form Actions

Retrieves actions for a form in Form.io.

```
GET https://connect.mindcloud.co/v1/universal/formio/latest/actions/list-form-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Form.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formio/latest/actions/list-form-actions?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formio/latest/actions/list-form-actions?${params}`, {
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
| `formId` | string | yes | The form ID to list actions for. |

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

Through the native Form.io API, this operation is `GET /form/:formId/action` (base URL `https://neabnzbnvbushtk.form.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-actions.md) for the provider-specific parameters and requirements.

