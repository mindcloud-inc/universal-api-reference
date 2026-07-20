# PubNub: Create Keyset

Creates a keyset in PubNub.

```
POST https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/create-keyset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/create-keyset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keyset.appId": "string",
  "keyset.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/create-keyset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keyset.appId": "string",
    "keyset.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `keyset.appId` | string | yes | The PubNub app ID that will own the keyset. |
| `keyset.name` | string | yes | The PubNub keyset name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "keyset": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object | The created keyset configuration. |
| `keyset` | object | The created keyset. |

## Native endpoint

Through the native PubNub API, this operation is `POST /keysets` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-keyset.md) for the provider-specific parameters and requirements.

