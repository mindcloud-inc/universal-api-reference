# Slack: Get List Item



```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-list-item?connectionId=$CONNECTION_ID&listId=F12345678&id=Rec12345678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "F12345678",
  "id": "Rec12345678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-list-item?${params}`, {
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
| `listId` | string | yes | Example: `F12345678`. |
| `id` | string | yes | Example: `Rec12345678`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeIsSubscribed` | boolean | no | Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Slack API returns.

## Native endpoint

Through the native Slack API, this operation is `POST slackLists.items.info` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-item.md) for the provider-specific parameters and requirements.

