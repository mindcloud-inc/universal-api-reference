# Timetonic: Get Book Messages

Retrieves messages for a book from Timetonic.

```
GET https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-book-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-book-messages?connectionId=$CONNECTION_ID&bookCode=table&bookOwner=mindcloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookCode": "table",
  "bookOwner": "mindcloud"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-book-messages?${params}`, {
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
| `bookCode` | string | yes | Book code to inspect. Default: `table`. |
| `bookOwner` | string | yes | Book owner to inspect. Default: `mindcloud`. |
| `syncStamp` | string | no | Optional sync stamp for incremental reads. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `smidFirst` | string | no | Optional lower message-id bound. |
| `smidLast` | string | no | Optional upper message-id bound. |
| `maxMessages` | string | no | Optional maximum number of messages to return. |
| `page` | string | no | Optional page number. |
| `searchString` | string | no | Optional free-text search string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "b_c": "string",
      "b_o": "string",
      "bookMessages": [
        {}
      ],
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
| `b_c` | string | Echoed book code. |
| `b_o` | string | Echoed book owner. |
| `bookMessages` | array<object> | Messages returned for the selected book. |
| `createdVNB` | string | TimeTonic backend version string. |
| `req` | string | Echoed provider request name. |
| `sstamp` | number | Provider sync stamp for the response. |
| `status` | string | Provider status for the book messages request. |
| `transactionId` | string | Provider transaction identifier for the request. |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-book-messages.md) for the provider-specific parameters and requirements.

