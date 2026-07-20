# Slack: List Channels

Retrieves channels from a Slack workspace.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-channels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-channels?${params}`, {
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
| `types` | list<string> | no | Accepts multiple values as an array. Default: `public_channel,private_channel`. |
| `sendAsBot` | boolean | no | Determines if this action should be performed by the current user or the Mindcloud bot. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `excludeArchived` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contextTeamId": "string",
      "created": "2026-05-07T12:00:00.000Z",
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
      "name": "Ava Chen",
      "nameNormalized": "Ava Chen",
      "numMembers": 1,
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
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contextTeamId` | string |  |
| `created` | date |  |
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
| `name` | string |  |
| `nameNormalized` | string |  |
| `numMembers` | number |  |
| `purpose.creator` | string |  |
| `purpose.lastSet` | number |  |
| `purpose.value` | string |  |
| `sharedTeamIds[]` | string |  |
| `topic.creator` | string |  |
| `topic.lastSet` | number |  |
| `topic.value` | string |  |
| `unlinked` | number |  |
| `updated` | date |  |

## Native endpoint

Through the native Slack API, this operation is `GET conversations.list` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

