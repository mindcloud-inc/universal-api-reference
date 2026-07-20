# Revel Digital: Get Schedule



```
GET https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-schedule?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-schedule?${params}`, {
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
| `id` | string | yes | Unique identifier of the schedule. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conditions": [
        {}
      ],
      "created_by_id": "string",
      "created_on": "string",
      "devices": [
        {}
      ],
      "end_date": "string",
      "end_time": "string",
      "friday": true,
      "group_id": "string",
      "group_name": "Ava Chen",
      "id": "string",
      "modified_by_id": "string",
      "modified_on": "string",
      "monday": true,
      "name": "Ava Chen",
      "playlist_id": "string",
      "priority": "string",
      "saturday": true,
      "start_date": "string",
      "start_time": "string",
      "sunday": true,
      "tags": "string",
      "template_id": "string",
      "thursday": true,
      "tuesday": true,
      "type": "string",
      "wednesday": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conditions` | array<object> |  |
| `created_by_id` | string |  |
| `created_on` | string |  |
| `devices` | array<object> |  |
| `end_date` | string |  |
| `end_time` | string |  |
| `friday` | boolean |  |
| `group_id` | string |  |
| `group_name` | string |  |
| `id` | string |  |
| `modified_by_id` | string |  |
| `modified_on` | string |  |
| `monday` | boolean |  |
| `name` | string |  |
| `playlist_id` | string |  |
| `priority` | string |  |
| `saturday` | boolean |  |
| `start_date` | string |  |
| `start_time` | string |  |
| `sunday` | boolean |  |
| `tags` | string |  |
| `template_id` | string |  |
| `thursday` | boolean |  |
| `tuesday` | boolean |  |
| `type` | string |  |
| `wednesday` | boolean |  |

## Native endpoint

Through the native Revel Digital API, this operation is `GET /schedules/:id` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule.md) for the provider-specific parameters and requirements.

