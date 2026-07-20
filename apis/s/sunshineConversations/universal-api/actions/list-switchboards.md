# Sunshine Conversations: List Switchboards

Retrieves app switchboards from Sunshine Conversations.

```
GET https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/list-switchboards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunshine Conversations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/list-switchboards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/list-switchboards?${params}`, {
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
| `appId` | string | no | Sunshine Conversations app id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "switchboards": [
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
| `switchboards` | array<object> | Switchboard records. |

## Native endpoint

Through the native Sunshine Conversations API, this operation is `GET /apps/:appId/switchboards` (base URL `https://api.smooch.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-switchboards.md) for the provider-specific parameters and requirements.

