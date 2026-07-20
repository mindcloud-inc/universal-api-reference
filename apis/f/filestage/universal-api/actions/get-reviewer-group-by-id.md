# Filestage: Get Reviewer Group by ID

Retrieves a reviewer group from Filestage by ID.

```
GET https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-reviewer-group-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-reviewer-group-by-id?connectionId=$CONNECTION_ID&stepId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stepId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-reviewer-group-by-id?${params}`, {
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
| `stepId` | string | yes | Step Id |

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

Through the native Filestage API, this operation is `GET /steps/{stepId}` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reviewer-group-by-id.md) for the provider-specific parameters and requirements.

