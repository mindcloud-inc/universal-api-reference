# Statistics Netherlands CBS: Get OData V4 Dimension

Retrieves a dimension from a Statistics Netherlands CBS dataset.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dimension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dimension?connectionId=$CONNECTION_ID&identifier=string&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string",
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dimension?${params}`, {
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
| `identifier` | string | yes | OData v4 dimension identifier, such as WijkenEnBuurten. |
| `tableIdentifier` | string | yes | CBS table identifier, such as 83765NED. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CodesUrl": "https://example.com",
      "ContainsCodes": true,
      "ContainsGroups": true,
      "Description": "string",
      "GroupsUrl": "https://example.com",
      "Identifier": "string",
      "Kind": "string",
      "MapYear": "string",
      "ReleasePolicy": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CodesUrl` | string | Dimension codes URL. |
| `ContainsCodes` | boolean | Whether code endpoint is available. |
| `ContainsGroups` | boolean | Whether group endpoint is available. |
| `Description` | string | Dimension description. |
| `GroupsUrl` | string | Dimension groups URL. |
| `Identifier` | string | Dimension identifier. |
| `Kind` | string | Dimension kind. |
| `MapYear` | string | Map year for geographic dimensions. |
| `ReleasePolicy` | string | Release policy. |
| `Title` | string | Dimension title. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Dimensions('{{identifier}}')` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-o-data-v4-dimension.md) for the provider-specific parameters and requirements.

