# SurveySparrow: Update Contact List

Updates an existing contact list in SurveySparrow.

```
PUT https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-contact-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-contact-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the contact list |
| `name` | string | no | Name of the contact list |
| `description` | string | no | Description of the contact list |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "contact_type_id": 1,
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `contact_type_id` | number |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `PATCH /contact_lists/{{id}}` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-list.md) for the provider-specific parameters and requirements.

