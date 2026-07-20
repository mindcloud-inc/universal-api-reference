# Statistics Netherlands CBS: List Feed Category Groups

Retrieves feed category groups from a Statistics Netherlands CBS table.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-feed-category-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-feed-category-groups?connectionId=$CONNECTION_ID&limit=25&offset=0&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-feed-category-groups?${params}`, {
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
| `tableIdentifier` | string | yes | CBS StatLine table identifier, such as 83765NED. |

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
| `Description` | string | Feed category group description. |
| `DimensionKey` | string | Dimension key. |
| `ID` | number | Feed category group id. |
| `ParentID` | number | Parent feed category group id. |
| `Title` | string | Feed category group title. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET /ODataFeed/odata/{{tableIdentifier}}/CategoryGroups` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-feed-category-groups.md) for the provider-specific parameters and requirements.

