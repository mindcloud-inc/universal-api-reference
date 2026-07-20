# Reamaze: Get Channel



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/get-channel?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/get-channel?${params}`, {
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
| `slug` | string | yes | Path parameter for slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brand": {},
      "channel": 1,
      "createdAt": "string",
      "email": "ava@example.com",
      "lastVerified": "string",
      "name": "Ava Chen",
      "replyFromOrigin": true,
      "settingsReplyFromName": "Ava Chen",
      "settingsSignature": "string",
      "slug": "string",
      "spamFilterEnabled": true,
      "updatedAt": "string",
      "verificationEmail": "ava@example.com",
      "verified": true,
      "visibility": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brand` | object |  |
| `channel` | number |  |
| `createdAt` | string |  |
| `email` | string |  |
| `lastVerified` | string |  |
| `name` | string |  |
| `replyFromOrigin` | boolean |  |
| `settingsReplyFromName` | string |  |
| `settingsSignature` | string |  |
| `slug` | string |  |
| `spamFilterEnabled` | boolean |  |
| `updatedAt` | string |  |
| `verificationEmail` | string |  |
| `verified` | boolean |  |
| `visibility` | number |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /channels/:slug` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

