# Userback: Update Feedback

Updates a Userback feedback item.

```
PUT https://connect.mindcloud.co/v1/universal/userback/latest/actions/update-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/userback/latest/actions/update-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedbackId": "7378423"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userback/latest/actions/update-feedback', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedbackId": "7378423"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedbackId` | number | yes | Feedback ID to update. Example: `7378423`. |
| `feedbackType` | string | no | Updated feedback type. Example: `General`. |
| `title` | string | no | Updated feedback title. Example: `MindCloud Stage 3 Feedback Updated`. |
| `description` | string | no | Updated feedback description. Example: `Updated by the Stage 3 build batch.`. |
| `pageUrl` | string | no | Updated page URL. Example: `https://mindcloud.co/stage-3-build-updated`. |
| `isShared` | boolean | no | Whether the feedback is shared. Default: `false`. |
| `allowPublicComment` | boolean | no | Whether public comments are allowed. Default: `false`. |
| `priority` | string | no | Updated priority. Example: `neutral`. |
| `category` | string | no | Updated category. Example: `Bug`. |
| `rating` | string | no | Updated rating. Example: `star_2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigneeId` | number | no | Updated assignee ID. Example: `105101`. |
| `dueDate` | date | no | Updated due date. Example: `2026-03-22`. |
| `notify` | boolean | no | Whether to notify subscribers about the update. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowPublicComment": true,
      "created": "string",
      "description": "string",
      "dueDate": "string",
      "email": "ava@example.com",
      "feedbackType": "string",
      "id": 1,
      "isPinned": true,
      "isPortalApproved": true,
      "isShared": true,
      "modified": "string",
      "name": "Ava Chen",
      "pageUrl": "https://example.com",
      "priority": "string",
      "projectId": 1,
      "rating": "string",
      "screenshots": [
        {
          "created": "string",
          "height": 1,
          "id": 1,
          "url": "https://example.com",
          "width": 1
        }
      ],
      "session": {
        "colorDepth": 1,
        "dpi": 1,
        "resolutionX": 1,
        "resolutionY": 1,
        "userAgent": "string",
        "windowHeight": 1,
        "windowWidth": 1
      },
      "shareUrl": "https://example.com",
      "title": "string",
      "userIdentification": "string",
      "voteCount": 1,
      "workflow": {
        "color": "string",
        "id": 1,
        "name": "Ava Chen",
        "sort": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowPublicComment` | boolean |  |
| `created` | string |  |
| `description` | string |  |
| `dueDate` | string |  |
| `email` | string |  |
| `feedbackType` | string |  |
| `id` | number |  |
| `isPinned` | boolean |  |
| `isPortalApproved` | boolean |  |
| `isShared` | boolean |  |
| `modified` | string |  |
| `name` | string |  |
| `pageUrl` | string |  |
| `priority` | string |  |
| `projectId` | number |  |
| `rating` | string |  |
| `screenshots[].created` | string |  |
| `screenshots[].height` | number |  |
| `screenshots[].id` | number |  |
| `screenshots[].url` | string |  |
| `screenshots[].width` | number |  |
| `session.colorDepth` | number |  |
| `session.dpi` | number |  |
| `session.resolutionX` | number |  |
| `session.resolutionY` | number |  |
| `session.userAgent` | string |  |
| `session.windowHeight` | number |  |
| `session.windowWidth` | number |  |
| `shareUrl` | string |  |
| `title` | string |  |
| `userIdentification` | string |  |
| `voteCount` | number |  |
| `workflow.color` | string |  |
| `workflow.id` | number |  |
| `workflow.name` | string |  |
| `workflow.sort` | number |  |

## Native endpoint

Through the native Userback API, this operation is `PATCH /feedback/:id` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-feedback.md) for the provider-specific parameters and requirements.

