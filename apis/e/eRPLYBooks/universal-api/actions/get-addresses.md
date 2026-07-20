# ERPLY Books: Get Addresses

Retrieves address records from ERPLY Books.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-addresses?${params}`, {
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
          "address2": "string",
          "addressID": 1,
          "city": "string",
          "country": "string",
          "lastModified": 1,
          "lastModifierEmployeeID": 1,
          "lastModifierUsername": "Ava Chen",
          "ownerID": 1,
          "postalCode": "string",
          "postcode": "string",
          "state": "string",
          "street": "string",
          "typeActivelyUsed": 1,
          "typeID": 1,
          "typeName": "Ava Chen"
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
| `records[].address2` | string |  |
| `records[].addressID` | number |  |
| `records[].city` | string |  |
| `records[].country` | string |  |
| `records[].lastModified` | number |  |
| `records[].lastModifierEmployeeID` | number |  |
| `records[].lastModifierUsername` | string |  |
| `records[].ownerID` | number |  |
| `records[].postalCode` | string |  |
| `records[].postcode` | string |  |
| `records[].state` | string |  |
| `records[].street` | string |  |
| `records[].typeActivelyUsed` | number |  |
| `records[].typeID` | number |  |
| `records[].typeName` | string |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-addresses.md) for the provider-specific parameters and requirements.

