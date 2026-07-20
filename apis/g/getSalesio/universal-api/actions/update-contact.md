# GetSales.io: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | UUID of the contact to update. |
| `firstName` | string | no | Contact first name. Example: `John`. |
| `lastName` | string | no | Contact last name. Example: `Doe`. |
| `companyName` | string | no | Contact company name. Example: `ExampleCorp`. |
| `email` | string | no | Contact email address. Example: `john.doe@example.com`. |
| `linkedin` | string | no | LinkedIn profile handle. Example: `john-doe-123456`. |
| `position` | string | no | Contact job title or position. Example: `Sales Manager`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email_status": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "list_uuid": "string",
      "name": "Ava Chen",
      "status": "string",
      "team_id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "work_email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `created_at` | date |  |
| `email_status` | string |  |
| `first_name` | string |  |
| `last_name` | string |  |
| `list_uuid` | string |  |
| `name` | string |  |
| `status` | string |  |
| `team_id` | number |  |
| `updated_at` | date |  |
| `uuid` | string |  |
| `work_email` | string |  |

## Native endpoint

Through the native GetSales.io API, this operation is `PUT /leads/api/leads/{uuid}` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

