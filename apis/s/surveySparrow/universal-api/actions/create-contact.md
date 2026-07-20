# SurveySparrow: Create Contact

Creates a new contact in SurveySparrow.

```
POST https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fullName` | string | no | Full name of the contact. |
| `email` | string | yes | Email address of the contact. |
| `contactType` | list | no | Type of contact. One of: `0`, `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phone` | string | no | Phone number of the contact. |
| `mobile` | string | no | Mobile number of the contact. |
| `jobTitle` | string | no | Job title of the contact. |
| `referenceId` | string | no | Reference ID of the contact. |
| `uniqueId` | string | no | Unique alphanumeric ID for the contact. |
| `unsubscribed` | boolean | no | Unsubscribed status of the contact. |
| `unsubscribeText` | string | no | Reason for unsubscribing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_type": "string",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "id": 1,
      "job_title": "string",
      "mobile": "string",
      "phone": "string",
      "reference_id": "string",
      "unique_id": "string",
      "unsubscribe_text": "string",
      "unsubscribed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_type` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `id` | number |  |
| `job_title` | string |  |
| `mobile` | string |  |
| `phone` | string |  |
| `reference_id` | string |  |
| `unique_id` | string |  |
| `unsubscribe_text` | string |  |
| `unsubscribed` | boolean |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `POST /contacts` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

