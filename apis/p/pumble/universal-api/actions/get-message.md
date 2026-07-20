# Pumble: Get Message

Retrieves a message from Pumble by ID.

```
GET https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pumble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-message?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-message?${params}`, {
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
| `channel` | string | no |  |
| `channelId` | string | no |  |
| `messageId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "channelId": "string",
      "deleted": true,
      "edited": true,
      "id": "string",
      "isFollowing": true,
      "savedTimestampMilli": 1,
      "subtype": "string",
      "text": "string",
      "timestamp": "string",
      "timestampMilli": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `channelId` | string |  |
| `deleted` | boolean |  |
| `edited` | boolean |  |
| `id` | string |  |
| `isFollowing` | boolean |  |
| `savedTimestampMilli` | number |  |
| `subtype` | string |  |
| `text` | string |  |
| `timestamp` | string |  |
| `timestampMilli` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Pumble API, this operation is `GET /fetchMessage` (base URL `https://pumble-api-keys.addons.marketplace.cake.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

