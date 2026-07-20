# GetSales.io: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/get-contact?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/get-contact?${params}`, {
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
| `uuid` | string | yes | UUID of the contact to retrieve. |

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

Through the native GetSales.io API, this operation is `GET /leads/api/leads/{uuid}` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

