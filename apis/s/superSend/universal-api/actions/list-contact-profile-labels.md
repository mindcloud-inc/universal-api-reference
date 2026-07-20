# SuperSend: List Contact Profile Labels

Retrieves profile labels for a SuperSend contact.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-contact-profile-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-contact-profile-labels?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-contact-profile-labels?${params}`, {
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
| `id` | string | yes | Resource ID (UUID) |
| `limit` | number | no | Default: 50. Range: 1 to 100. |
| `offset` | number | no | Default: 0. Range: 0 to inf. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applies_to": "string",
      "color": "string",
      "contact_profile_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "label_id": "string",
      "label_team_id": "string",
      "name": "Ava Chen",
      "object": "string",
      "org_id": "string",
      "team_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applies_to` | string |  |
| `color` | string |  |
| `contact_profile_id` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `label_id` | string |  |
| `label_team_id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `org_id` | string |  |
| `team_id` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /contacts/{id}/profile-labels` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-profile-labels.md) for the provider-specific parameters and requirements.

