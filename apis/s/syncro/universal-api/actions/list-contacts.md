# Syncro: List Contacts

Retrieves a list of contacts from Syncro.

```
GET https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/list-contacts?${params}`, {
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
| `customerId` | number | no | Any contacts attached to a Customer ID. |
| `page` | number | no | Returns the provided page of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {
          "accountId": 1,
          "address1": "string",
          "city": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "customerId": 1,
          "email": "ava@example.com",
          "id": 1,
          "name": "Ava Chen",
          "optOut": true,
          "phone": "string",
          "processedPhone": "string",
          "sinceUpdatedAt": "2026-05-07T12:00:00.000Z",
          "state": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "meta": {
        "page": 1,
        "perPage": 1,
        "totalEntries": 1,
        "totalPages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts[].accountId` | number |  |
| `contacts[].address1` | string |  |
| `contacts[].city` | string |  |
| `contacts[].createdAt` | date |  |
| `contacts[].customerId` | number |  |
| `contacts[].email` | string |  |
| `contacts[].id` | number |  |
| `contacts[].name` | string |  |
| `contacts[].optOut` | boolean |  |
| `contacts[].phone` | string |  |
| `contacts[].processedPhone` | string |  |
| `contacts[].sinceUpdatedAt` | date |  |
| `contacts[].state` | string |  |
| `contacts[].updatedAt` | date |  |
| `meta.page` | number |  |
| `meta.perPage` | number |  |
| `meta.totalEntries` | number |  |
| `meta.totalPages` | number |  |

## Native endpoint

Through the native Syncro API, this operation is `GET /contacts` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

