# SurveySparrow: Update Contact Property

Updates an existing contact property in SurveySparrow.

```
PUT https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-contact-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-contact-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-contact-property', {
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
| `id` | number | yes | ID of the contact property |
| `type` | list | no | Type of contact property |
| `label` | string | no | Label of the contact property |
| `description` | string | no | Description of the contact property |
| `contactPropertyGroupId` | number | no | Contact property group ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_property_group_id": 1,
      "contact_type_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "label": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_property_group_id` | number |  |
| `contact_type_id` | number |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `label` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `PATCH /contact_properties/{{id}}` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-property.md) for the provider-specific parameters and requirements.

