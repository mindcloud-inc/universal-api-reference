# SuperSend: Assign Label to Contact Profile

Assigns a profile label to a SuperSend contact.

```
POST https://connect.mindcloud.co/v1/universal/superSend/latest/actions/assign-label-to-contact-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/assign-label-to-contact-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "labelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/assign-label-to-contact-profile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "labelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Resource ID (UUID) |
| `labelId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_profile_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "label_id": "string",
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
| `contact_profile_id` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `label_id` | string |  |
| `object` | string |  |
| `org_id` | string |  |
| `team_id` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `POST /contacts/{id}/profile-labels` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-label-to-contact-profile.md) for the provider-specific parameters and requirements.

