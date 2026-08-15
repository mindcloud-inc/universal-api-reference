# Samsara: Update Driver



```
PATCH https://connect.mindcloud.co/v1/universal/samsara/latest/actions/update-driver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X PATCH "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/update-driver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/samsara/latest/actions/update-driver', {
  method: 'PATCH',
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
| `externalIds` | object<object> | no |  |
| `name` | string<object> | no |  |
| `password` | string<object> | no |  |
| `tagIds[]` | array<string> | no |  |
| `username` | string<string> | no |  |
| `driverId` | string | no |  |
| `driverActivationStatus` | string | no |  |
| `deactivatedAtTime` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Samsara API returns.

## Native endpoint

Through the native Samsara API, this operation is `PATCH fleet/drivers/:driverId` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/update-driver.md) for the provider-specific parameters and requirements.

