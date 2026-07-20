# Vibrato: Retrieve task template

Retrieves a specific task template from Vibrato.

```
GET https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-task-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vibrato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-task-template?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-task-template?${params}`, {
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
| `uuid` | string | yes | UUID from Vibrato. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "call_locale": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "featured": true,
      "iconoir_icon": "string",
      "public": true,
      "recipient_country_code": "string",
      "recipient_name": "Ava Chen",
      "recipient_phone_number": "string",
      "tags": [
        "string"
      ],
      "task_description": "string",
      "task_instructions": "string",
      "task_name": "Ava Chen",
      "task_properties": [
        {}
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `call_locale` | string |  |
| `created_at` | date |  |
| `featured` | boolean |  |
| `iconoir_icon` | string |  |
| `public` | boolean |  |
| `recipient_country_code` | string |  |
| `recipient_name` | string |  |
| `recipient_phone_number` | string |  |
| `tags` | array<string> |  |
| `task_description` | string |  |
| `task_instructions` | string |  |
| `task_name` | string |  |
| `task_properties` | array<object> |  |
| `updated_at` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Vibrato API, this operation is `GET /task_templates/{uuid}/` (base URL `https://api.getvibrato.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-task-template.md) for the provider-specific parameters and requirements.

