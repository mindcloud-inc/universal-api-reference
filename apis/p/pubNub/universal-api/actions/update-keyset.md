# PubNub: Update Keyset

Updates an existing keyset in PubNub.

```
PUT https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/update-keyset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/update-keyset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/update-keyset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The PubNub keyset ID. |
| `name` | string | yes | The updated PubNub keyset name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "publishKey": "string",
      "subscribeKey": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string | The owning app ID. |
| `createdAt` | date | When the keyset was created. |
| `id` | string | The keyset ID. |
| `name` | string | The keyset name. |
| `publishKey` | string | The publish key. |
| `subscribeKey` | string | The subscribe key. |
| `type` | string | The keyset type. |
| `updatedAt` | date | When the keyset was last updated. |

## Native endpoint

Through the native PubNub API, this operation is `PATCH /keysets/:id` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-keyset.md) for the provider-specific parameters and requirements.

