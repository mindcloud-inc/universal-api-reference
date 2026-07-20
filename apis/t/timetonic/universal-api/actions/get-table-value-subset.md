# Timetonic: Get Table Value Subset

Retrieves a subset of table values from Timetonic.

```
GET https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-table-value-subset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-table-value-subset?connectionId=$CONNECTION_ID&bookOwner=mindcloud&categoryId=651531&fieldIds=8729679%2C8729681&rowIds=147159906%2C147159938" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookOwner": "mindcloud",
  "categoryId": "651531",
  "fieldIds": "8729679,8729681",
  "rowIds": "147159906,147159938"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-table-value-subset?${params}`, {
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
| `bookOwner` | string | yes | Owner of the target book. Default: `mindcloud`. |
| `categoryId` | string | yes | Table/category id to read from. Default: `651531`. |
| `fieldIds` | string | yes | Comma-separated field ids to return. Default: `8729679,8729681`. |
| `rowIds` | string | yes | Comma-separated row ids to return. Default: `147159906,147159938`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "catId": 1,
      "createdVNB": "string",
      "req": "string",
      "sstamp": 1,
      "status": "string",
      "tableValues": [
        [
          "string"
        ]
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
| `catId` | number | Echoed table/category id. |
| `createdVNB` | string | TimeTonic backend version string. |
| `req` | string | Echoed provider request name. |
| `sstamp` | number | Provider sync stamp for the response. |
| `status` | string | Provider status for the subset request. |
| `tableValues` | array<array> | Subset values returned for the requested rows and fields. |
| `transactionId` | string | Provider transaction identifier for the request. |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table-value-subset.md) for the provider-specific parameters and requirements.

