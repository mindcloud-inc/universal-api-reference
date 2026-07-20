# Statistics Netherlands CBS: Get Table

Retrieves a table from Statistics Netherlands CBS.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-table?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-table?${params}`, {
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
| `id` | number | yes | Numeric CBS catalog table ID. Required by the OData key path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ApiUrl": "https://example.com",
      "ColumnCount": 1,
      "FeedUrl": "https://example.com",
      "ID": 1,
      "Identifier": "string",
      "Language": "string",
      "RecordCount": 1,
      "ShortTitle": "string",
      "Summary": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ApiUrl` | string |  |
| `ColumnCount` | number |  |
| `FeedUrl` | string |  |
| `ID` | number |  |
| `Identifier` | string |  |
| `Language` | string |  |
| `RecordCount` | number |  |
| `ShortTitle` | string |  |
| `Summary` | string |  |
| `Title` | string |  |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET /ODataCatalog/Tables({{id}})` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table.md) for the provider-specific parameters and requirements.

