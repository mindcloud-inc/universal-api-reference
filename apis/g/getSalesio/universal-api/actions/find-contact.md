# GetSales.io: Find Contact



```
GET https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/find-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/find-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/find-contact?${params}`, {
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
| `linkedinId` | string | no | LinkedIn URL, handle, or ID used to identify the contact. Example: `john-doe-123456`. |
| `email` | string | no | Email address used to identify the contact. Example: `john.doe@example.com`. |
| `name` | string | no | Contact name used with company name for lookup. Example: `John Doe`. |
| `companyName` | string | no | Company name used with contact name for lookup. Example: `Example Inc.`. |
| `disableAggregation` | boolean | no | When true, disables contact data aggregation. Default: `false`. |

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

Through the native GetSales.io API, this operation is `POST /leads/api/leads/lookup-one` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-contact.md) for the provider-specific parameters and requirements.

