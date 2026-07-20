# Slack: Create Channel

Creates a new channel in Slack.

```
POST https://connect.mindcloud.co/v1/universal/slack/latest/actions/create-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slack/latest/actions/create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/create-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the public or private channel to create |
| `isPrivate` | boolean | no | Create a private channel instead of a public one |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendAsBot` | boolean | no | Determines if this action should be performed by the current user or the Mindcloud bot. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contextTeamId": "string",
      "created": 1,
      "creator": "string",
      "id": "string",
      "isArchived": true,
      "isChannel": true,
      "isExtShared": true,
      "isGeneral": true,
      "isGroup": true,
      "isIm": true,
      "isMember": true,
      "isMpim": true,
      "isOrgShared": true,
      "isPendingExtShared": true,
      "isPrivate": true,
      "isShared": true,
      "lastRead": "string",
      "name": "Ava Chen",
      "nameNormalized": "Ava Chen",
      "parentConversation": {},
      "priority": 1,
      "purpose": {
        "creator": "string",
        "lastSet": 1,
        "value": "string"
      },
      "sharedTeamIds": [
        "string"
      ],
      "topic": {
        "creator": "string",
        "lastSet": 1,
        "value": "string"
      },
      "unlinked": 1,
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contextTeamId` | string |  |
| `created` | number |  |
| `creator` | string |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `isChannel` | boolean |  |
| `isExtShared` | boolean |  |
| `isGeneral` | boolean |  |
| `isGroup` | boolean |  |
| `isIm` | boolean |  |
| `isMember` | boolean |  |
| `isMpim` | boolean |  |
| `isOrgShared` | boolean |  |
| `isPendingExtShared` | boolean |  |
| `isPrivate` | boolean |  |
| `isShared` | boolean |  |
| `lastRead` | string |  |
| `name` | string |  |
| `nameNormalized` | string |  |
| `parentConversation` | object |  |
| `priority` | number |  |
| `purpose.creator` | string |  |
| `purpose.lastSet` | number |  |
| `purpose.value` | string |  |
| `sharedTeamIds[]` | string |  |
| `topic.creator` | string |  |
| `topic.lastSet` | number |  |
| `topic.value` | string |  |
| `unlinked` | number |  |
| `updated` | number |  |

## Native endpoint

Through the native Slack API, this operation is `POST conversations.create` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-channel.md) for the provider-specific parameters and requirements.

