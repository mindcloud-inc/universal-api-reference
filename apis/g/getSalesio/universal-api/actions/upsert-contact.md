# GetSales.io: Create Or Update Contact



```
POST https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/upsert-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/upsert-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lead.linkedinId": "john-doe-123456",
  "listUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/upsert-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lead.linkedinId": "john-doe-123456",
    "listUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lead.linkedinId` | string | yes | Contact LinkedIn ID or profile handle. Example: `john-doe-123456`. |
| `lead.email` | string | no | Contact email address. Example: `john.doe@example.com`. |
| `lead.firstName` | string | no | Contact first name. Example: `John`. |
| `lead.lastName` | string | no | Contact last name. Example: `Doe`. |
| `lead.companyName` | string | no | Contact company name. Example: `ExampleCorp`. |
| `listUuid` | string | yes | UUID of the target list. |
| `updateIfExists` | boolean | no | When true, updates the contact if it already exists. Default: `true`. |
| `moveToList` | boolean | no | When true, moves an existing contact to the specified list. |

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

Through the native GetSales.io API, this operation is `POST /leads/api/leads/upsert` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-contact.md) for the provider-specific parameters and requirements.

