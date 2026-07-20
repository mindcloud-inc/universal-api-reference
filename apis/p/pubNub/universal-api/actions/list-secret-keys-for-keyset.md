# PubNub: List Secret Keys For Keyset

Retrieves secret keys for a PubNub keyset.

```
GET https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/list-secret-keys-for-keyset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PubNub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/list-secret-keys-for-keyset?connectionId=$CONNECTION_ID&keysetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keysetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/list-secret-keys-for-keyset?${params}`, {
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
| `keysetId` | string | yes | The PubNub keyset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "secretKeys": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `secretKeys` | array<object> | The secret keys for the keyset. |

## Native endpoint

Through the native PubNub API, this operation is `GET /keysets/:keysetId/secret-keys` (base URL `https://admin-api.pubnub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-secret-keys-for-keyset.md) for the provider-specific parameters and requirements.

