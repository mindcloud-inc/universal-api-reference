# SurveySparrow: Create Contact Property

Creates a new contact property in SurveySparrow.

```
POST https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-contact-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-contact-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-contact-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | list | yes | Type of contact property |
| `label` | string | yes | Label of the contact property |
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

Through the native SurveySparrow API, this operation is `POST /contact_properties` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-property.md) for the provider-specific parameters and requirements.

