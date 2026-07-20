# ClickSend SMS: List Contacts

Retrieves contacts from a ClickSend SMS list.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&list_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "list_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-contacts?${params}`, {
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
| `list_id` | number | yes | List identifier. |
| `page` | number | no | Page number. |
| `limit` | number | no | Items per page. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updatedAfter` | number | no | Unix timestamp lower bound. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "addressCity": "string",
          "addressCountry": "string",
          "addressLine1": "string",
          "addressLine2": "string",
          "addressPostalCode": "string",
          "addressState": "string",
          "contactId": 1,
          "custom1": "string",
          "custom2": "string",
          "custom3": "string",
          "custom4": "string",
          "dateAdded": {},
          "dateUpdated": {},
          "email": "ava@example.com",
          "faxNumber": "string",
          "firstName": "Ava",
          "lastName": "Chen",
          "listId": 1,
          "listName": "Ava Chen",
          "organizationName": "Ava Chen",
          "phoneNumber": "string"
        }
      ],
      "from": 1,
      "lastPage": 1,
      "nextPageUrl": {},
      "perPage": 1,
      "prevPageUrl": {},
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data[].addressCity` | string |  |
| `data[].addressCountry` | string |  |
| `data[].addressLine1` | string |  |
| `data[].addressLine2` | string |  |
| `data[].addressPostalCode` | string |  |
| `data[].addressState` | string |  |
| `data[].contactId` | number |  |
| `data[].custom1` | string |  |
| `data[].custom2` | string |  |
| `data[].custom3` | string |  |
| `data[].custom4` | string |  |
| `data[].dateAdded` | object |  |
| `data[].dateUpdated` | object |  |
| `data[].email` | string |  |
| `data[].faxNumber` | string |  |
| `data[].firstName` | string |  |
| `data[].lastName` | string |  |
| `data[].listId` | number |  |
| `data[].listName` | string |  |
| `data[].organizationName` | string |  |
| `data[].phoneNumber` | string |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `GET /v3/lists/:list_id/contacts` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

