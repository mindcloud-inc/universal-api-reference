# Freshdesk: List Contacts

Retrieves a list of contacts from Freshdesk.

```
GET https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/list-contacts?${params}`, {
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
| `email` | string | no |  |
| `mobile` | string | no |  |
| `phone` | string | no |  |
| `companyId` | list<number> | no |  |
| `state` | list<string> | no | One of: `blocked`, `deleted`, `unverified`, `verified`. |
| `contactType` | list<string> | no | One of: `contact`, `visitor`. |
| `updatedSince` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "companyId": 1,
      "contactType": "string",
      "createdAt": "string",
      "deleted": true,
      "email": "ava@example.com",
      "id": 1,
      "mobile": "string",
      "name": "Ava Chen",
      "phone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `companyId` | number |  |
| `contactType` | string |  |
| `createdAt` | string |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `id` | number |  |
| `mobile` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Freshdesk API, this operation is `GET /contacts` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

