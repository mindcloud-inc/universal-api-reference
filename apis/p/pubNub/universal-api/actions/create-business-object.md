# PubNub: Create Business Object

Creates a business object in PubNub Illuminate.

```
POST https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/create-business-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/create-business-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields[0].jsonFieldType": "TEXT",
  "fields[0].jsonPath": "$.message.body.event",
  "fields[0].name": "Event",
  "fields[0].source": "JSONPATH",
  "fields[1].jsonFieldType": "NUMERIC",
  "fields[1].jsonPath": "$.message.body.data.player_id",
  "fields[1].name": "Player ID",
  "fields[1].source": "JSONPATH",
  "isActive": "false",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/create-business-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields[0].jsonFieldType": "TEXT",
    "fields[0].jsonPath": "$.message.body.event",
    "fields[0].name": "Event",
    "fields[0].source": "JSONPATH",
    "fields[1].jsonFieldType": "NUMERIC",
    "fields[1].jsonPath": "$.message.body.data.player_id",
    "fields[1].name": "Player ID",
    "fields[1].source": "JSONPATH",
    "isActive": "false",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Business object description. |
| `fields[0].jsonFieldType` | string | yes | Field type for the first field. Default: `TEXT`. |
| `fields[0].jsonPath` | string | yes | JSONPath for the first field. Default: `$.message.body.event`. |
| `fields[0].name` | string | yes | Name for the first business object field. Default: `Event`. |
| `fields[0].source` | string | yes | Field source type for the first field. Default: `JSONPATH`. |
| `fields[1].jsonFieldType` | string | yes | Field type for the second field. Default: `NUMERIC`. |
| `fields[1].jsonPath` | string | yes | JSONPath for the second field. Default: `$.message.body.data.player_id`. |
| `fields[1].name` | string | yes | Name for the second business object field. Default: `Player ID`. |
| `fields[1].source` | string | yes | Field source type for the second field. Default: `JSONPATH`. |
| `isActive` | boolean | yes | Whether the business object starts capturing data. Default: `false`. |
| `name` | string | yes | Business object name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PubNub API returns.

## Native endpoint

Through the native PubNub API, this operation is `POST /illuminate/business-objects` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-business-object.md) for the provider-specific parameters and requirements.

