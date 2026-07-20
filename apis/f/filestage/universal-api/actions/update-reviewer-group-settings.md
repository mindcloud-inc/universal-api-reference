# Filestage: Update Reviewer Group Settings

Updates settings for a Filestage reviewer group.

```
PUT https://connect.mindcloud.co/v1/universal/filestage/latest/actions/update-reviewer-group-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/update-reviewer-group-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stepId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/update-reviewer-group-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stepId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stepId` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `downloadInReview` | boolean | no | If you this setting is false, the download button won't be visible for reviewers file status is `In Review`. Default: `true`. |
| `downloadNeedsChanges` | boolean | no | If you this setting is false, the download button won't be visible for reviewers file has been marked as `Need Changes`. Default: `true`. |
| `downloadApproved` | boolean | no | If you this setting is false, the download button won't be visible for reviewers file has been approved. Default: `true`. |
| `commentInReview` | boolean | no | If you this is set as false, reviewers cannot create, edit or delete comments when the review status is `In review`. Default: `true`. |
| `commentNeedsChanges` | boolean | no | If you this is set as false, reviewers cannot create, edit or delete comments when the review status is `Needs Changes` Default: `false`. |
| `commentApproved` | boolean | no | If you this is set as false, reviewers cannot create, edit or delete comments when the file has been approved. Default: `false`. |
| `emailNotifications` | boolean | no | If you this setting is set as false, reviewers without a registered account will no longer receive email notifications for project activities (new comments, new files and versions, file status changes and submitted reviews). Default: `false`. |
| `passwordProtection` | boolean | no | When this setting is true, any new reviewers without a Filestage account will need to enter the password as specified in the `password` field Default: `false`. |
| `uploadingEnabled` | boolean | no | If this setting is set as `true`, external reviewers will be able to upload new files and new versions to this reviewer group. Default: `false`. |
| `anonymousReviewers` | boolean | no | If you this setting as `true`, all reviewers will be anonymous to each other. Default: `false`. |
| `password` | string | no | This field is required when `passwordProtection` is set as `true`. It creates a password to protect this reviewer group. |

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

Through the native Filestage API, this operation is `PUT /steps/{stepId}/settings` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reviewer-group-settings.md) for the provider-specific parameters and requirements.

