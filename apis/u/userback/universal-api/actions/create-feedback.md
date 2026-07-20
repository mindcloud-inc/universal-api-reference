# Userback: Create Feedback

Creates a new feedback item in Userback.

```
POST https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "137605",
  "feedbackType": "General",
  "title": "App feedback from MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "137605",
    "feedbackType": "General",
    "title": "App feedback from MindCloud"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Feedback project ID. Example: `137605`. |
| `feedbackType` | string | yes | Feedback type value. Example: `General`. |
| `title` | string | yes | Feedback title. Example: `App feedback from MindCloud`. |
| `description` | string | no | Feedback description. Example: `Created by the Stage 3 build batch.`. |
| `email` | string | no | Feedback submitter email. Example: `apps@mindcloud.co`. |
| `name` | string | no | Feedback submitter name. Example: `MindCloud Batch Runner`. |
| `pageUrl` | string | no | Page URL for the feedback. Example: `https://mindcloud.co/stage-3-build`. |
| `isShared` | boolean | no | Whether the feedback is shared. Default: `false`. |
| `allowPublicComment` | boolean | no | Whether public comments are allowed. Default: `false`. |
| `priority` | string | no | Feedback priority. Example: `neutral`. |
| `category` | string | no | Feedback category. Example: `Bug`. |
| `rating` | string | no | Feedback rating. Example: `star_2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigneeId` | number | no | Assignee member ID. Example: `105101`. |
| `dueDate` | date | no | Due date for the feedback. Example: `2026-03-31`. |
| `notify` | boolean | no | Whether to send notifications. Default: `false`. |

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

Through the native Userback API, this operation is `POST /feedback` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-feedback.md) for the provider-specific parameters and requirements.

