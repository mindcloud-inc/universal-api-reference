# ADP: Create Time Card



```
POST https://connect.mindcloud.co/v1/universal/adp/latest/actions/create-time-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ADP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/adp/latest/actions/create-time-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/adp/latest/actions/create-time-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `associateOID` | string | no |  |
| `workAssignmentID` | string | no |  |
| `startTime` | date | no |  |
| `endTime` | date | no |  |
| `entryTypeCode` | list<string> | no | - dayPeriodEntry -> Used for employee whose the presence is declared in day period (morning, afternoon, fullday). - hoursEntry -> Used for employee whose the presence is declared in duration. - timePairEntry -> Used for employee whose the presence is declared in slice time. Default: `timePairEntry`. |
| `duration` | number | no | indicate how many minutes were worked. INT -> 150 = 2 hours and 30 minutes Default: `0`. |
| `dayPeriodCode` | list<string> | no | Default: `morning`. |
| `entryCode` | string | no | what type of entry is being saved (service, meal, shop, tip, etc) Example: `TIPS, MEAL, SERVICE, SHOPPING, DRIVING, ETC`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ADP API returns.

## Native endpoint

Through the native ADP API, this operation is `POST events/time/v2/time-entries.modify` (base URL `https://api.adp.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-card.md) for the provider-specific parameters and requirements.

