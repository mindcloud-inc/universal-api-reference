# Statistics Netherlands CBS: Get Category Group

Retrieves a category group from a Statistics Netherlands CBS table.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-category-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-category-group?connectionId=$CONNECTION_ID&id=1&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-category-group?${params}`, {
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
| `id` | number | yes | Numeric category group row ID. Required by the OData key path. |
| `tableIdentifier` | string | yes | CBS StatLine table identifier, for example 83765NED. Required by the service path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Description": "string",
      "DimensionKey": "string",
      "ID": 1,
      "ParentID": 1,
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Description` | string | Category group description. |
| `DimensionKey` | string | Dimension key. |
| `ID` | number | Category group id. |
| `ParentID` | number | Parent category group id. |
| `Title` | string | Category group title. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET /ODataApi/odata/{{tableIdentifier}}/CategoryGroups({{id}})` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category-group.md) for the provider-specific parameters and requirements.

