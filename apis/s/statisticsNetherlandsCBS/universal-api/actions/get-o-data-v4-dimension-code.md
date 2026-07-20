# Statistics Netherlands CBS: Get OData V4 Dimension Code

Retrieves a dimension code from a Statistics Netherlands CBS dataset.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dimension-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dimension-code?connectionId=$CONNECTION_ID&dimensionIdentifier=string&identifier=string&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dimensionIdentifier": "string",
  "identifier": "string",
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dimension-code?${params}`, {
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
| `identifier` | string | yes | OData v4 dimension code identifier, such as NL00. |
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

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/{{dimensionIdentifier}}Codes('{{identifier}}')` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-o-data-v4-dimension-code.md) for the provider-specific parameters and requirements.

