# Streamtime: List Company Contacts



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-company-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-company-contacts?connectionId=$CONNECTION_ID&companyId=711949" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "711949"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-company-contacts?${params}`, {
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
| `companyId` | number | yes | Company ID Example: `711949`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "companyId": 1,
      "contactStatus": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "notes": "string",
      "phoneNumber": "string",
      "position": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Is contact active |
| `companyId` | number | Company ID |
| `contactStatus` | object | Contact status |
| `email` | string | Email address |
| `firstName` | string | First name |
| `id` | number | Contact ID |
| `lastName` | string | Last name |
| `notes` | string | Notes |
| `phoneNumber` | string | Phone number |
| `position` | string | Position |

## Native endpoint

Through the native Streamtime API, this operation is `GET /companies/:company_id/contacts` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-contacts.md) for the provider-specific parameters and requirements.

