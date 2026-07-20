# Filestage: Add Reviewers to Reviewer Group

Adds reviewers to a Filestage reviewer group.

```
POST https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-reviewers-to-reviewer-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-reviewers-to-reviewer-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stepId": "string",
  "reviewerEmails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-reviewers-to-reviewer-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stepId": "string",
    "reviewerEmails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stepId` | string | yes | Step Id |
| `reviewerEmails[]` | array<string> | yes | This is an array of collaborators' emails. This can only contain the emails of existing team members |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | no | This is a custom message that would be sent to invited reviewers. |
| `notifyEmail` | boolean | no | When `true` a notification email would be sent to the invited reviewers and when `false` no emails are sent. |
| `requestDecision` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "reviewers": {
        "email": "ava@example.com",
        "reviewDecisionRequested": true
      },
      "reviewLink": "https://example.com",
      "settings": {
        "anonymousReviewers": true,
        "commentApproved": true,
        "commentInReview": true,
        "commentNeedsChanges": true,
        "downloadApproved": true,
        "downloadInReview": true,
        "downloadNeedsChanges": true,
        "emailNotifications": true,
        "password": "string",
        "passwordProtection": true,
        "uploadingEnabled": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `reviewers` | array<object> |  |
| `reviewers.email` | string |  |
| `reviewers.reviewDecisionRequested` | boolean |  |
| `reviewLink` | string |  |
| `settings` | object |  |
| `settings.anonymousReviewers` | boolean |  |
| `settings.commentApproved` | boolean |  |
| `settings.commentInReview` | boolean |  |
| `settings.commentNeedsChanges` | boolean |  |
| `settings.downloadApproved` | boolean |  |
| `settings.downloadInReview` | boolean |  |
| `settings.downloadNeedsChanges` | boolean |  |
| `settings.emailNotifications` | boolean |  |
| `settings.password` | string |  |
| `settings.passwordProtection` | boolean |  |
| `settings.uploadingEnabled` | boolean |  |

## Native endpoint

Through the native Filestage API, this operation is `POST /steps/{stepId}/reviewers` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-reviewers-to-reviewer-group.md) for the provider-specific parameters and requirements.

