# Filestage: Add Reviewer Group to Project Template

Creates a reviewer group in a Filestage project template.

```
POST https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-reviewer-group-to-project-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-reviewer-group-to-project-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectTemplateId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-reviewer-group-to-project-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectTemplateId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectTemplateId` | string | yes | ID of the project template |
| `name` | string | yes | The name of the reviewer group. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `settings.downloadInReview` | boolean | no | If you this setting is false, the download button won't be visible for reviewers file status is `In Review`. Default: `true`. |
| `settings.downloadNeedsChanges` | boolean | no | If you this setting is false, the download button won't be visible for reviewers file has been marked as `Need Changes`. Default: `true`. |
| `settings.downloadApproved` | boolean | no | If you this setting is false, the download button won't be visible for reviewers file has been approved. Default: `true`. |
| `settings.commentInReview` | boolean | no | If you this is set as false, reviewers cannot create, edit or delete comments when the review status is `In review`. Default: `true`. |
| `settings.commentNeedsChanges` | boolean | no | If you this is set as false, reviewers cannot create, edit or delete comments when the review status is `Needs Changes` Default: `false`. |
| `settings.commentApproved` | boolean | no | If you this is set as false, reviewers cannot create, edit or delete comments when the file has been approved. Default: `false`. |
| `settings.emailNotifications` | boolean | no | If you this setting is set as false, reviewers without a registered account will no longer receive email notifications for project activities (new comments, new files and versions, file status changes and submitted reviews). Default: `false`. |
| `settings.passwordProtection` | boolean | no | When this setting is true, any new reviewers without a Filestage account will need to enter the password as specified in the `password` field Default: `false`. |
| `settings.uploadingEnabled` | boolean | no | If this setting is set as `true`, external reviewers will be able to upload new files and new versions to this reviewer group. Default: `false`. |
| `settings.anonymousReviewers` | boolean | no | If you this setting as `true`, all reviewers will be anonymous to each other. Default: `false`. |
| `settings.password` | string | no | This field is required when `passwordProtection` is set as `true`. It creates a password to protect this reviewer group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Filestage API returns.

## Native endpoint

Through the native Filestage API, this operation is `POST /project-templates/{projectTemplateId}/steps` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-reviewer-group-to-project-template.md) for the provider-specific parameters and requirements.

