# ProProfs Project: List Clients

Retrieves a list of clients from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-clients?${params}`, {
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
| `clientName` | string | no | Simple wildcard client-name search. |
| `limit` | string | no | Limit the number of returned clients. |
| `offset` | string | no | Offset for returned clients. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "active": "string",
          "address": "string",
          "background": "string",
          "city": "string",
          "clientId": "string",
          "clientName": "Ava Chen",
          "contactId": "string",
          "country": "string",
          "dateCreated": "string",
          "dateModified": "string",
          "email": "ava@example.com",
          "fax": "string",
          "mobile": "string",
          "postcode": "string",
          "state": "string",
          "tel": "string",
          "userId": "string",
          "website": "string"
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
| `data[].active` | string |  |
| `data[].address` | string |  |
| `data[].background` | string |  |
| `data[].city` | string |  |
| `data[].clientId` | string |  |
| `data[].clientName` | string |  |
| `data[].contactId` | string |  |
| `data[].country` | string |  |
| `data[].dateCreated` | string |  |
| `data[].dateModified` | string |  |
| `data[].email` | string |  |
| `data[].fax` | string |  |
| `data[].mobile` | string |  |
| `data[].postcode` | string |  |
| `data[].state` | string |  |
| `data[].tel` | string |  |
| `data[].userId` | string |  |
| `data[].website` | string |  |
| `paging.limit` | number |  |
| `paging.offset` | number |  |
| `paging.totalRecords` | number |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /clients` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

