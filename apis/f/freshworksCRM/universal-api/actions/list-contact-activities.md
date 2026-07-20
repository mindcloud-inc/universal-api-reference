# Freshworks CRM: List Contact Activities

Retrieves activities for a contact in Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-contact-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-contact-activities?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-contact-activities?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": [
        [
          {}
        ]
      ],
      "meta": {
        "has_next": true,
        "has_previous": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities[]` | array<object> |  |
| `activities[].action_type` | string |  |
| `activities[].actionable_id` | number |  |
| `activities[].actionable_type` | string |  |
| `activities[].created_at` | date |  |
| `activities[].id` | string |  |
| `activities[].targetable_id` | number |  |
| `activities[].targetable_type` | string |  |
| `activities[].user_activity` | boolean |  |
| `meta.has_next` | boolean |  |
| `meta.has_previous` | boolean |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET /api/contacts/:id/activities` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-activities.md) for the provider-specific parameters and requirements.

