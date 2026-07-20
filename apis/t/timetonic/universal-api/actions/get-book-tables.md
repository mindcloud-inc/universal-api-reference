# Timetonic: Get Book Tables

Retrieves tables for a book from Timetonic.

```
GET https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-book-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-book-tables?connectionId=$CONNECTION_ID&bookCode=table&bookOwner=mindcloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookCode": "table",
  "bookOwner": "mindcloud"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-book-tables?${params}`, {
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
| `format` | string | no | Optional response format. Use android to include detailed table metadata. Default: `android`. |
| `includeFields` | string | no | Optional flag to include field metadata. Default: `true`. |
| `includeEnums` | string | no | Optional flag to include field enum metadata. Default: `true`. |
| `getRowIds` | string | no | Optional flag to include view-to-row associations when using android format with field metadata. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externViews` | string | no | Optional flag to include external views. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookTables": [
        {}
      ],
      "createdVNB": "string",
      "req": "string",
      "sstamp": 1,
      "status": "string",
      "tabs": [
        {}
      ],
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookTables` | array<object> | Tables returned for the selected book. |
| `createdVNB` | string | TimeTonic backend version string. |
| `req` | string | Echoed provider request name. |
| `sstamp` | number | Provider sync stamp for the response. |
| `status` | string | Provider status for the book tables request. |
| `tabs` | array<object> | Tab metadata returned for the selected book. |
| `transactionId` | string | Provider transaction identifier for the request. |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-book-tables.md) for the provider-specific parameters and requirements.

