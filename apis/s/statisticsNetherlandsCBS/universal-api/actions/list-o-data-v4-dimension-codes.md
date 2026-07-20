# Statistics Netherlands CBS: List OData V4 Dimension Codes

Retrieves dimension codes from a Statistics Netherlands CBS dataset.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-dimension-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-dimension-codes?connectionId=$CONNECTION_ID&dimensionIdentifier=string&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dimensionIdentifier": "string",
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-dimension-codes?${params}`, {
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
| `dimensionIdentifier` | string | yes | OData v4 dimension identifier prefix, such as WijkenEnBuurten. |
| `tableIdentifier` | string | yes | CBS table identifier, such as 83765NED. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Description": "string",
      "DetailRegionCode": "string",
      "DimensionGroupId": "string",
      "Identifier": "string",
      "Index": 1,
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Description` | string | Dimension code description. |
| `DetailRegionCode` | string | Detailed regional code when present. |
| `DimensionGroupId` | string | Dimension group id. |
| `Identifier` | string | Dimension code identifier. |
| `Index` | number | Ordering index. |
| `Title` | string | Dimension code title. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/{{dimensionIdentifier}}Codes` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-o-data-v4-dimension-codes.md) for the provider-specific parameters and requirements.

