# ERPLY Books: Get Customer Groups

Retrieves customer groups from ERPLY Books.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-customer-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-customer-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-customer-groups?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "records": [
        {
          "added": 1,
          "clientGroupID": 1,
          "customerGroupID": 1,
          "lastModified": 1,
          "name": "Ava Chen",
          "parentID": 1,
          "pricelistID": 1,
          "pricelistID2": 1,
          "pricelistID3": 1,
          "pricelistID4": 1,
          "pricelistID5": 1
        }
      ],
      "status": {
        "errorCode": 1,
        "generationTime": 1,
        "recordsInResponse": 1,
        "recordsTotal": 1,
        "request": "string",
        "requestUnixTime": 1,
        "responseStatus": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records[].added` | number |  |
| `records[].clientGroupID` | number |  |
| `records[].customerGroupID` | number |  |
| `records[].lastModified` | number |  |
| `records[].name` | string |  |
| `records[].parentID` | number |  |
| `records[].pricelistID` | number |  |
| `records[].pricelistID2` | number |  |
| `records[].pricelistID3` | number |  |
| `records[].pricelistID4` | number |  |
| `records[].pricelistID5` | number |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-groups.md) for the provider-specific parameters and requirements.

