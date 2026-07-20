# Moosend: Create Segment

Creates a new empty segment in Moosend.

```
POST https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailingListId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moosend/latest/actions/create-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailingListId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailingListId` | string | yes | The ID of the email list where the segment is created. |
| `name` | string | yes | The name of the segment. |
| `matchType` | string | no | Specifies how subscribers are returned by your segment based on matching criteria: All (Default) - returns subscribers that match all the given criteria. Any - returns subscribers that match any of the given criteria. |
| `fetchType` | string | no | Specifies how many criteria-matching subscribers are contained in your segment: All - returns all criteria matching subscribers. Top - returns only a maximum number of subscribers defined in FetchValue . TopPercent - returns only a percentage of subscribers defined in FetchValue . |
| `fetchValue` | number | no | Specifies the maximum number for FetchType:Top or percentage for FetchType:TopPercent of members to be contained in the created segment. If not specified, 0 is assumed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Moosend API returns.

## Native endpoint

Through the native Moosend API, this operation is `POST /lists/{{MailingListID}}/segments/create.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-segment.md) for the provider-specific parameters and requirements.

