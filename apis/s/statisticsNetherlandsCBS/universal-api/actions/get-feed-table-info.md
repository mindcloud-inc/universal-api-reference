# Statistics Netherlands CBS: Get Feed Table Info

Retrieves feed table info from a Statistics Netherlands CBS table.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-feed-table-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-feed-table-info?connectionId=$CONNECTION_ID&id=1&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-feed-table-info?${params}`, {
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
| `id` | number | yes | Numeric TableInfos row ID. |
| `tableIdentifier` | string | yes | CBS StatLine table identifier, such as 83765NED. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Catalog": "string",
      "Frequency": "string",
      "ID": 1,
      "Identifier": "string",
      "Language": "string",
      "Period": "string",
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
| `Catalog` | string |  |
| `Frequency` | string |  |
| `ID` | number |  |
| `Identifier` | string |  |
| `Language` | string |  |
| `Period` | string |  |
| `ShortTitle` | string |  |
| `Summary` | string |  |
| `Title` | string |  |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET /ODataFeed/odata/{{tableIdentifier}}/TableInfos({{id}})` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed-table-info.md) for the provider-specific parameters and requirements.

