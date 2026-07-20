# Vibrato: Update task template

Updates an existing task template in Vibrato.

```
PUT https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/update-task-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vibrato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/update-task-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/update-task-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | UUID from Vibrato. |
| `taskName` | string | no | Task template name. |
| `taskDescription` | string | no | Task template description. |
| `taskInstructions` | string | no | Instructions for the task template. |
| `taskProperties[]` | array<object> | no | Task property definitions. |
| `recipientName` | string | no | Default recipient name. |
| `recipientPhoneNumber` | string | no | Default recipient phone number. |
| `recipientCountryCode` | string | no | Default recipient country code. |
| `callLocale` | string | no | Default call locale. |
| `public` | boolean | no | Whether the template is public. |
| `featured` | boolean | no | Whether the template is featured. |
| `tags[]` | array<string> | no | Tags. |
| `iconoirIcon` | string | no | Iconoir icon name. |

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

Through the native Vibrato API, this operation is `PATCH /task_templates/{uuid}/` (base URL `https://api.getvibrato.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-template.md) for the provider-specific parameters and requirements.

