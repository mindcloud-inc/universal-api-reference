# Statistics Netherlands CBS: List Feed Resource Rows

Retrieves feed resource rows from a Statistics Netherlands CBS table.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-feed-resource-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-feed-resource-rows?connectionId=$CONNECTION_ID&limit=25&offset=0&resourceName=Ava%20Chen&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "resourceName": "Ava Chen",
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-feed-resource-rows?${params}`, {
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
| `resourceName` | string | yes | Named entity set in the feed service, such as a dimension resource. Required by the service path. |
| `tableIdentifier` | string | yes | CBS StatLine table identifier, for example 83765NED. Required by the feed service path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CategoryGroupID": 1,
      "Description": "string",
      "DetailRegionCode": "string",
      "Key": "string",
      "Municipality": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CategoryGroupID` | number | Category group ID when present. |
| `Description` | string | Feed resource row description. |
| `DetailRegionCode` | string | Detailed region code when present. |
| `Key` | string | Feed resource row key. |
| `Municipality` | string | Municipality code when present. |
| `Title` | string | Feed resource row title. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET /ODataFeed/odata/{{tableIdentifier}}/{{resourceName}}` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-feed-resource-rows.md) for the provider-specific parameters and requirements.

