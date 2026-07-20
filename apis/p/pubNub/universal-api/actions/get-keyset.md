# PubNub: Get Keyset

Retrieves a keyset from PubNub.

```
GET https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/get-keyset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/get-keyset?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/get-keyset?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The PubNub keyset ID. |

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

Through the native PubNub API, this operation is `GET /keysets/:id` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-keyset.md) for the provider-specific parameters and requirements.

