# ProProfs Project: List Contacts

Retrieves a list of contacts from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-contacts?${params}`, {
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
| `clientId` | string | no | Show contacts for a particular client. |
| `limit` | string | no | Limit the number of returned contacts. |
| `offset` | string | no | Offset for returned contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "clientId": "string",
          "companyName": "Ava Chen",
          "contactId": "string",
          "contactName": "Ava Chen",
          "dateCreated": "string",
          "dateModified": "string",
          "email": "ava@example.com",
          "fax": "string",
          "mobile": "string",
          "role": "string",
          "tel": "string",
          "userId": "string"
        }
      ],
      "paging": {
        "limit": 1,
        "offset": 1,
        "totalRecords": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].clientId` | string |  |
| `data[].companyName` | string |  |
| `data[].contactId` | string |  |
| `data[].contactName` | string |  |
| `data[].dateCreated` | string |  |
| `data[].dateModified` | string |  |
| `data[].email` | string |  |
| `data[].fax` | string |  |
| `data[].mobile` | string |  |
| `data[].role` | string |  |
| `data[].tel` | string |  |
| `data[].userId` | string |  |
| `paging.limit` | number |  |
| `paging.offset` | number |  |
| `paging.totalRecords` | number |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /contacts` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

