# Timetonic: Get Table Value Comments

Retrieves comments for a table value from Timetonic.

```
GET https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-table-value-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-table-value-comments?connectionId=$CONNECTION_ID&bookOwner=mindcloud&rowId=147159056&fieldId=8729209" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookOwner": "mindcloud",
  "rowId": "147159056",
  "fieldId": "8729209"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-table-value-comments?${params}`, {
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
| `bookOwner` | string | yes | Book owner containing the row. Default: `mindcloud`. Example: `mindcloud`. |
| `rowId` | string | yes | Row identifier containing the field value. Example: `147159056`. |
| `fieldId` | string | yes | Field identifier whose comments should be fetched. Example: `8729209`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdVNB": "string",
      "data": {},
      "fieldId": 1,
      "req": "string",
      "rowId": 1,
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
| `createdVNB` | string |  |
| `data` | object |  |
| `fieldId` | number |  |
| `req` | string |  |
| `rowId` | number |  |
| `sstamp` | number |  |
| `status` | string |  |
| `transactionId` | string |  |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table-value-comments.md) for the provider-specific parameters and requirements.

