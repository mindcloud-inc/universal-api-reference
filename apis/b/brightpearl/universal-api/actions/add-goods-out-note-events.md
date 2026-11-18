# Brightpearl: Add Goods-Out Note Events



```
POST https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/add-goods-out-note-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/add-goods-out-note-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "goodsOutNoteId": 1,
  "events[]": [
    {}
  ],
  "events[].eventCode": "PAC",
  "events[].occured": "2026-05-07T12:00:00.000Z",
  "events[].eventOwnerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/add-goods-out-note-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "goodsOutNoteId": 1,
    "events[]": [{}],
    "events[].eventCode": "PAC",
    "events[].occured": "2026-05-07T12:00:00.000Z",
    "events[].eventOwnerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `goodsOutNoteId` | number | yes |  |
| `lastEventVersion` | string | no | Use lastEventVersion from Goods-Out Note GET to prevent duplicate events. |
| `events[]` | array<object> | yes |  |
| `events[].eventCode` | list<string> | yes | One of: `PAC`, `PIC`, `PRI`, `SHW`, `UPA`, `UPI`, `UPR`. |
| `events[].occured` | date | yes | Brightpearl spells this request field occured. |
| `events[].eventOwnerId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Brightpearl API returns.

## Native endpoint

Through the native Brightpearl API, this operation is `POST /warehouse-service/goods-note/goods-out/:goodsOutNoteId/event` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-goods-out-note-events.md) for the provider-specific parameters and requirements.

