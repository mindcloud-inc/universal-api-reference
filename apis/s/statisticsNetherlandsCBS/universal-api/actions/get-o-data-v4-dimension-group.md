# Statistics Netherlands CBS: Get OData V4 Dimension Group

Retrieves a dimension group from a Statistics Netherlands CBS dataset.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dimension-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dimension-group?connectionId=$CONNECTION_ID&dimensionIdentifier=string&id=string&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dimensionIdentifier": "string",
  "id": "string",
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-dimension-group?${params}`, {
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
| `id` | string | yes | OData v4 dimension group id, such as WBGM. |
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
| `Description` | string | Dimension group description. |
| `Id` | string | Dimension group id. |
| `Index` | number | Ordering index. |
| `ParentId` | string | Parent dimension group id. |
| `Title` | string | Dimension group title. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/{{dimensionIdentifier}}Groups('{{id}}')` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-o-data-v4-dimension-group.md) for the provider-specific parameters and requirements.

