# PubNub: Rotate Secret Key

Rotates a secret key for a PubNub keyset.

```
PUT https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/rotate-secret-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/rotate-secret-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keysetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/rotate-secret-key', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keysetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `keysetId` | string | yes | The PubNub keyset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "secretKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `secretKey` | string | The new permanent secret key. |

## Native endpoint

Through the native PubNub API, this operation is `POST /keysets/:keysetId/secret-keys` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rotate-secret-key.md) for the provider-specific parameters and requirements.

