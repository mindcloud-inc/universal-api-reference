# Moosend: Update Segment

Updates an existing segment in Moosend.

```
PUT https://connect.mindcloud.co/v1/universal/moosend/latest/actions/update-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/update-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailingListId": "string",
  "segmentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moosend/latest/actions/update-segment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailingListId": "string",
    "segmentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailingListId` | string | yes | The ID of the email list that contains the segment. |
| `segmentId` | string | yes | The ID of the segment to be updated. |
| `name` | string | no | The name of the segment. If not specified, the existing name is retained. |
| `matchType` | string | no | Specifies how subscribers are returned by your segment based on matching criteria. If not specified, All is assumed. All (Default) - returns subscribers that match all the given criteria. Any - returns subscribers that match any of the given criteria. |
| `fetchType` | string | no | Specifies how many criteria-matching subscribers are contained in your segment. If not specified, All is assumed. All - returns all criteria matching subscribers. Top - returns only a maximum number of subscribers defined in FetchValue . TopPercent - returns only a percentage of subscribers defined in FetchValue . |
| `fetchValue` | number | no | Specifies the maximum number for FetchType:Top or percentage for FetchType:TopPercent of members to be contained in the created segment. If not specified, 0 is assumed. |
| `criteria` | list<object> | no | An array containing the criteria parameters used to filter the email list. If not specified, existing criteria are retained. Field - the criterion used to filter the email list. See Field values . Comparer - the operator that defines how to compare a Field with its Value . See Comparer values . Value - the search term used to filter the specified Field . LastXMinutes - constrains the results by the time that has elapsed. DateFrom to DateTo - constrains the results by a date span. Date Function - the value used with custom fields of dateTime data type. See DateFunction values . |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Moosend API returns.

## Native endpoint

Through the native Moosend API, this operation is `POST /lists/{{MailingListID}}/segments/{{SegmentID}}/update.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-segment.md) for the provider-specific parameters and requirements.

