# Statistics Netherlands CBS: List OData V4 Measure Groups

Retrieves measure groups from a Statistics Netherlands CBS dataset.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-measure-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-measure-groups?connectionId=$CONNECTION_ID&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-measure-groups?${params}`, {
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
      "Description": "string",
      "Id": "string",
      "Index": 1,
      "ParentId": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Description` | string | Measure group description. |
| `Id` | string | Measure group id. |
| `Index` | number | Ordering index. |
| `ParentId` | string | Parent measure group id. |
| `Title` | string | Measure group title. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/MeasureGroups` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-o-data-v4-measure-groups.md) for the provider-specific parameters and requirements.

