# PubNub: Update Secret Key Expiration Time

Updates secret key expiration time in PubNub.

```
PUT https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/update-secret-key-expiration-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/update-secret-key-expiration-time" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keysetId": "string",
  "secretKeyPrefix": "string",
  "expiresAt": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/update-secret-key-expiration-time', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keysetId": "string",
    "secretKeyPrefix": "string",
    "expiresAt": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `keysetId` | string | yes | The PubNub keyset ID. |
| `secretKeyPrefix` | string | yes | The rotated secret key prefix in sec-c-xxxxx format. |
| `expiresAt` | date | yes | The new expiration time for the rotated secret key. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PubNub API returns.

## Native endpoint

Through the native PubNub API, this operation is `PATCH /keysets/:keysetId/secret-keys/:secretKeyPrefix` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-secret-key-expiration-time.md) for the provider-specific parameters and requirements.

