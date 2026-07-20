# SureContact: Update Contact

Updates an existing contact in SureContact.

```
PUT https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactUuid` | string | yes | The UUID of the contact. |
| `customFields` | object | no | Custom field values keyed by field name. |
| `metadata` | object | no | Additional metadata as key-value pairs. |
| `primaryFields` | object | no | Primary contact information. |
| `primaryFields.company` | string | no | The contact company name. |
| `primaryFields.email` | string | no | The contact email address. |
| `primaryFields.firstName` | string | no | The contact first name. |
| `primaryFields.jobTitle` | string | no | The contact job title. |
| `primaryFields.lastName` | string | no | The contact last name. |
| `primaryFields.phone` | string | no | The contact phone number. |
| `primaryFields.status` | string | no | The contact status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "do_not_email": true,
      "email": "ava@example.com",
      "email_status": "ava@example.com",
      "first_name": "Ava",
      "formal_name": "Ava Chen",
      "full_name": "Ava Chen",
      "job_title": "string",
      "language": "string",
      "last_activity_at": "2026-05-07T12:00:00.000Z",
      "last_name": "Chen",
      "source": "string",
      "source_label": "string",
      "status": "string",
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
| `company` | string |  |
| `created_at` | date |  |
| `do_not_email` | boolean |  |
| `email` | string |  |
| `email_status` | string |  |
| `first_name` | string |  |
| `formal_name` | string |  |
| `full_name` | string |  |
| `job_title` | string |  |
| `language` | string |  |
| `last_activity_at` | date |  |
| `last_name` | string |  |
| `source` | string |  |
| `source_label` | string |  |
| `status` | string |  |
| `updated_at` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native SureContact API, this operation is `PUT api/v1/public/contacts/:contact_uuid` (base URL `https://api.surecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

