# Zoho Cliq: Remove Channel Members

Removes members from a Zoho Cliq channel.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/remove-channel-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/remove-channel-members?connectionId=$CONNECTION_ID&channelId=string&userIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string",
  "userIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/remove-channel-members?${params}`, {
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
| `channelId` | string | yes | The ID of the channel where members should be removed. |
| `userIds[]` | array<string> | yes | The user IDs to remove from the channel. |
| `silent` | boolean | no | When true, remove members without sending notifications. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Cliq API returns.

## Native endpoint

Through the native Zoho Cliq API, this operation is `DELETE /channels/:channelId/members` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-channel-members.md) for the provider-specific parameters and requirements.

