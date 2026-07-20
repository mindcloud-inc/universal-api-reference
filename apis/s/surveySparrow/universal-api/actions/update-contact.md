# SurveySparrow: Update Contact

Updates an existing contact in SurveySparrow.

```
PUT https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-contact', {
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
| `id` | number | yes | ID of the contact. |
| `fullName` | string | no | Full name of the contact. |
| `email` | string | no | Email address of the contact. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phone` | string | no | Phone number of the contact. |
| `mobile` | string | no | Mobile number of the contact. |
| `jobTitle` | string | no | Job title of the contact. |
| `referenceId` | string | no | Reference ID of the contact. |
| `uniqueId` | string | no | Unique alphanumeric ID for the contact. |
| `unsubscribeText` | string | no | Reason for unsubscribing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "active": true,
      "contact_lists": [
        {}
      ],
      "contact_type": "string",
      "createddate": {},
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "job_title": "string",
      "last_name": "Chen",
      "manager_id": {},
      "mobile": {},
      "name": "Ava Chen",
      "preferred_channels": [
        {}
      ],
      "shared_token": "string",
      "signup_token": "string",
      "unique_id": "string",
      "unsubscribed": true,
      "unsubscribed_at": {},
      "updated_at": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `active` | boolean |  |
| `contact_lists` | array<object> |  |
| `contact_type` | string |  |
| `createddate` | object |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `job_title` | string |  |
| `last_name` | string |  |
| `manager_id` | object |  |
| `mobile` | object |  |
| `name` | string |  |
| `preferred_channels` | array<object> |  |
| `shared_token` | string |  |
| `signup_token` | string |  |
| `unique_id` | string |  |
| `unsubscribed` | boolean |  |
| `unsubscribed_at` | object |  |
| `updated_at` | object |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `PUT /contacts/{{id}}` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

