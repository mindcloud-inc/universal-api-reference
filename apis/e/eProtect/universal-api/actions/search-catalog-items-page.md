# 3E Protect: Search Catalog Items Page



```
GET https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/search-catalog-items-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/search-catalog-items-page?connectionId=$CONNECTION_ID&pageNumber=1&pageSize=100" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageNumber": "1",
  "pageSize": "100"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/search-catalog-items-page?${params}`, {
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
| `lastAlteredDate` | object | no |  |
| `lastAlteredDate.valueMin` | string | no | Inclusive start of the fixed change-date window, formatted as an ISO 8601 timestamp. |
| `lastAlteredDate.valueMax` | string | no | End of the fixed change-date window. Keep this value unchanged while reading its subsequent pages. |
| `lastAlteredDate.compareOption` | list | no | One of: `0`, `1`, `2`, `3`, `4`, `5`. |
| `pageNumber` | number | yes | The explicit 3E page number, starting at 1. |
| `pageSize` | number | yes | Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "listOfItems": [
        {
          "country": "string",
          "documentLink": "https://example.com",
          "emeaExposureScenario": "string",
          "language": "string",
          "manufacturerName": "Ava Chen",
          "manufacturerPartNumber": "string",
          "productName": "Ava Chen",
          "productUid": "string",
          "revisionDate": "string"
        }
      ],
      "moreRecords": true,
      "pageNumber": 1,
      "pageSize": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `listOfItems[].country` | string |  |
| `listOfItems[].documentLink` | string |  |
| `listOfItems[].emeaExposureScenario` | string |  |
| `listOfItems[].language` | string |  |
| `listOfItems[].manufacturerName` | string |  |
| `listOfItems[].manufacturerPartNumber` | string |  |
| `listOfItems[].productName` | string |  |
| `listOfItems[].productUid` | string |  |
| `listOfItems[].revisionDate` | string |  |
| `moreRecords` | boolean |  |
| `pageNumber` | number |  |
| `pageSize` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native 3E Protect API, this operation is `POST {{credentials.documentSearchApiBaseUrl}}/document-search` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-catalog-items-page.md) for the provider-specific parameters and requirements.

