# Slack: Get Channel Information

Retrieves conversation details from a Slack workspace.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-channel-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-channel-information?connectionId=$CONNECTION_ID&channel=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-channel-information?${params}`, {
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
| `channel` | list<string> | yes | Conversation ID to learn more about |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeLocale` | boolean | no | Set this to true to receive the locale for this conversation. |
| `includeMemberCount` | boolean | no | Set to true to include the member count for the specified conversation. |

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
      "isNonThreadable": true,
      "isOrgShared": true,
      "isPendingExtShared": true,
      "isPrivate": true,
      "isReadOnly": true,
      "isShared": true,
      "isThreadOnly": true,
      "lastRead": "string",
      "name": "Ava Chen",
      "nameNormalized": "Ava Chen",
      "parentConversation": {},
      "properties": {
        "tabs": [
          {
            "id": "string",
            "label": "string",
            "type": "string"
          }
        ],
        "tabz": [
          {
            "type": "string"
          }
        ]
      },
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
| `isNonThreadable` | boolean |  |
| `isOrgShared` | boolean |  |
| `isPendingExtShared` | boolean |  |
| `isPrivate` | boolean |  |
| `isReadOnly` | boolean |  |
| `isShared` | boolean |  |
| `isThreadOnly` | boolean |  |
| `lastRead` | string |  |
| `name` | string |  |
| `nameNormalized` | string |  |
| `parentConversation` | object |  |
| `properties.tabs[].id` | string |  |
| `properties.tabs[].label` | string |  |
| `properties.tabs[].type` | string |  |
| `properties.tabz[].type` | string |  |
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

Through the native Slack API, this operation is `GET conversations.info` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-information.md) for the provider-specific parameters and requirements.

