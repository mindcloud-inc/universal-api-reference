# Statistics Netherlands CBS: Get Feed Resource Row

Retrieves a feed resource row from a Statistics Netherlands CBS table.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-feed-resource-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-feed-resource-row?connectionId=$CONNECTION_ID&key=string&resourceName=Ava%20Chen&tableIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string",
  "resourceName": "Ava Chen",
  "tableIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-feed-resource-row?${params}`, {
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
| `key` | string | yes | The string Key value for the row in the named feed resource. |
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

Through the native Statistics Netherlands CBS API, this operation is `GET /ODataFeed/odata/{{tableIdentifier}}/{{resourceName}}('{{key}}')` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed-resource-row.md) for the provider-specific parameters and requirements.

