# ERPLY Books: Get Currencies

Retrieves currency records from ERPLY Books.

```
GET https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ERPLY Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eRPLYBooks/latest/actions/get-currencies?${params}`, {
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
          "added": "string",
          "code": "string",
          "currencyID": "string",
          "default": "string",
          "lastModified": "string",
          "name": "Ava Chen",
          "nameFraction": "Ava Chen",
          "nameShort": "Ava Chen",
          "prefix": "string",
          "rate": "string",
          "suffix": "string"
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
| `records[].added` | string |  |
| `records[].code` | string |  |
| `records[].currencyID` | string |  |
| `records[].default` | string |  |
| `records[].lastModified` | string |  |
| `records[].name` | string |  |
| `records[].nameFraction` | string |  |
| `records[].nameShort` | string |  |
| `records[].prefix` | string |  |
| `records[].rate` | string |  |
| `records[].suffix` | string |  |
| `status.errorCode` | number |  |
| `status.generationTime` | number |  |
| `status.recordsInResponse` | number |  |
| `status.recordsTotal` | number |  |
| `status.request` | string |  |
| `status.requestUnixTime` | number |  |
| `status.responseStatus` | string |  |

## Native endpoint

Through the native ERPLY Books API, this operation is `POST /` (base URL `https://{{credentials.customerCode}}.erply.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-currencies.md) for the provider-specific parameters and requirements.

