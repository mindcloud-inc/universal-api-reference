# Statistics Netherlands CBS: List OData V4 Dimensions

Retrieves dimensions from a Statistics Netherlands CBS dataset.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-dimensions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-dimensions?connectionId=$CONNECTION_ID&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-dimensions?${params}`, {
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

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Dimensions` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-o-data-v4-dimensions.md) for the provider-specific parameters and requirements.

