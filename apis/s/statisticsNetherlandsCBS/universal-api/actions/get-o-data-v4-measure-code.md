# Statistics Netherlands CBS: Get OData V4 Measure Code

Retrieves a measure code from a Statistics Netherlands CBS dataset.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-measure-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-measure-code?connectionId=$CONNECTION_ID&identifier=string&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string",
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-measure-code?${params}`, {
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
| `identifier` | string | yes | OData v4 measure code identifier, such as GM000C. |
| `tableIdentifier` | string | yes | CBS table identifier, such as 83765NED. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "DataType": "string",
      "Decimals": 1,
      "Description": "string",
      "Identifier": "string",
      "Index": 1,
      "MeasureGroupId": "string",
      "PresentationType": "string",
      "Title": "string",
      "Unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DataType` | string | Value data type. |
| `Decimals` | number | Number of decimal places. |
| `Description` | string | Measure code description. |
| `Identifier` | string | Measure code identifier. |
| `Index` | number | Ordering index. |
| `MeasureGroupId` | string | Parent measure group id. |
| `PresentationType` | string | Presentation type. |
| `Title` | string | Measure code title. |
| `Unit` | string | Measure unit. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/MeasureCodes('{{identifier}}')` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-o-data-v4-measure-code.md) for the provider-specific parameters and requirements.

