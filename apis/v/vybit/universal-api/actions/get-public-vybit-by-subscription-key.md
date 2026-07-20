# Vybit: Get Public Vybit by Subscription Key



```
GET https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-public-vybit-by-subscription-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-public-vybit-by-subscription-key?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/get-public-vybit-by-subscription-key?${params}`, {
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
| `key` | string | yes | The subscription key for the public vybit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "following": true,
      "imageUrl": "https://example.com",
      "key": "string",
      "linkUrl": "https://example.com",
      "name": "Ava Chen",
      "ownerName": "Ava Chen",
      "soundKey": "string",
      "soundType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `following` | boolean |  |
| `imageUrl` | string |  |
| `key` | string |  |
| `linkUrl` | string |  |
| `name` | string |  |
| `ownerName` | string |  |
| `soundKey` | string |  |
| `soundType` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Vybit API, this operation is `GET /subscription/{{key}}` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-public-vybit-by-subscription-key.md) for the provider-specific parameters and requirements.

