# Timetonic: Get All Books Info

Retrieves information for all books from Timetonic.

```
GET https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-all-books-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-all-books-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-all-books-info?${params}`, {
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
| `syncStamp` | string | no | Optional sync stamp for incremental reads. |
| `bookCode` | string | no | Optional book code to narrow the response. |
| `bookOwner` | string | no | Optional book owner to narrow the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allBooks": {},
      "createdVNB": "string",
      "req": "string",
      "sstamp": 1,
      "status": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allBooks` | object | Books and contacts payload returned by TimeTonic. |
| `createdVNB` | string | TimeTonic backend version string. |
| `req` | string | Echoed provider request name. |
| `sstamp` | number | Provider sync stamp for the response. |
| `status` | string | Provider status for the books request. |
| `transactionId` | string | Provider transaction identifier for the request. |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-books-info.md) for the provider-specific parameters and requirements.

