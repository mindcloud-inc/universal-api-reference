# Pumble: Search Messages

Finds messages in Pumble by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/pumble/latest/actions/search-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pumble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/search-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pumble/latest/actions/search-messages?${params}`, {
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
| `from[]` | array<string> | no | Array of user identifiers or names to filter search results by sender. |
| `in[]` | array<string> | no | Array of channel or conversation identifiers to search within. |
| `text` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {
        "author": "string",
        "channelId": "string",
        "deleted": true,
        "edited": true,
        "id": "string",
        "isFollowing": true,
        "subtype": "string",
        "text": "string",
        "timestamp": "string",
        "timestampMilli": 1,
        "workspaceId": "string"
      },
      "hasMore": true,
      "totalElements": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content.author` | string |  |
| `content.channelId` | string |  |
| `content.deleted` | boolean |  |
| `content.edited` | boolean |  |
| `content.id` | string |  |
| `content.isFollowing` | boolean |  |
| `content.subtype` | string |  |
| `content.text` | string |  |
| `content.timestamp` | string |  |
| `content.timestampMilli` | number |  |
| `content.workspaceId` | string |  |
| `hasMore` | boolean |  |
| `totalElements` | number |  |

## Native endpoint

Through the native Pumble API, this operation is `POST /searchMessages` (base URL `https://pumble-api-keys.addons.marketplace.cake.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-messages.md) for the provider-specific parameters and requirements.

