# Statistics Netherlands CBS: List Table Infos

Retrieves table info from a Statistics Netherlands CBS table.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-table-infos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-table-infos?connectionId=$CONNECTION_ID&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-table-infos?${params}`, {
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
| `tableIdentifier` | string | yes | CBS StatLine table identifier, for example 83765NED. Required by the service path. |

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

Through the native Statistics Netherlands CBS API, this operation is `GET /ODataApi/odata/{{tableIdentifier}}/TableInfos` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-table-infos.md) for the provider-specific parameters and requirements.

