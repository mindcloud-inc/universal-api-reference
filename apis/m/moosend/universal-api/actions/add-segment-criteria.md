# Moosend: Add Segment Criteria

Adds criteria to a segment in Moosend.

```
PUT https://connect.mindcloud.co/v1/universal/moosend/latest/actions/add-segment-criteria
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/add-segment-criteria" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailingListId": "string",
  "segmentId": "string",
  "field": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moosend/latest/actions/add-segment-criteria', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailingListId": "string",
    "segmentId": "string",
    "field": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailingListId` | string | yes | The ID of the email list that contains the segment. |
| `segmentId` | string | yes | The ID of the segment. |
| `field` | string | yes | The criterion used to filter the email list. See Field values . |
| `comparer` | string | no | The operator that defines how to compare a Field with its Value . See Comparer values . |
| `value` | string | no | The search term used to filter the specified Field . |
| `lastXMinutes` | number | no | Constrains the results by the time that has elapsed. |
| `dateFrom` | date | no | Constrains the results by a date span. |
| `dateTo` | date | no | Constrains the results by a date span. |
| `dateFunction` | string | no | The value used with custom fields of dateTime data type. See DateFunction values. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Moosend API returns.

## Native endpoint

Through the native Moosend API, this operation is `POST /lists/{{MailingListID}}/segments/{{SegmentID}}/criteria/add.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-segment-criteria.md) for the provider-specific parameters and requirements.

