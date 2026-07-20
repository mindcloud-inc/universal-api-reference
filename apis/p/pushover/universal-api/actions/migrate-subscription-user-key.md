# Pushover: Migrate Subscription User Key



```
POST https://connect.mindcloud.co/v1/universal/pushover/latest/actions/migrate-subscription-user-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/migrate-subscription-user-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscription": "string",
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushover/latest/actions/migrate-subscription-user-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscription": "string",
    "user": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscription` | string | yes | Subscription code identifying which subscription to migrate into. |
| `user` | string | yes | Existing Pushover user key to migrate. |
| `deviceName` | string | no | Optional device name to limit the resulting subscription to one device. |
| `sound` | string | no | Optional preferred default sound to store with the subscription. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "request": "string",
      "status": 1,
      "subscribedUserKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request` | string | Pushover request identifier. |
| `status` | number | API status. Returns 1 when the subscription user key migration succeeds. |
| `subscribedUserKey` | string | New subscribed user key returned by the migration endpoint. |

## Native endpoint

Through the native Pushover API, this operation is `POST /subscriptions/migrate.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/migrate-subscription-user-key.md) for the provider-specific parameters and requirements.

