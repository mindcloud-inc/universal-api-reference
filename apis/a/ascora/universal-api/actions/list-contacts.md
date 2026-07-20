# Ascora: List Contacts

Retrieves contacts from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-contacts?${params}`, {
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
| `filterText` | string | no | Contains search across contact details. |
| `phoneNumber` | string | no | Exact match across phone and mobile after removing spaces. |
| `pageSize` | number | no | Result page size. |
| `page` | number | no | Page number to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Matching contact records. |
| `success` | boolean | Whether Ascora returned the contacts search successfully. |
| `totalPages` | number | Total result pages returned by Ascora. |
| `totalRecords` | number | Total matching contacts. |

## Native endpoint

Through the native Ascora API, this operation is `GET /Customers/Contacts` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

