# Calibre: Create Pull Request Review

Creates a new pull request review in Calibre.

```
POST https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-pull-request-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-pull-request-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.site": "string",
  "variables.title": "string",
  "variables.sha": "string",
  "variables.branch": "string",
  "variables.url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-pull-request-review', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.site": "string",
    "variables.title": "string",
    "variables.sha": "string",
    "variables.branch": "string",
    "variables.url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.site` | string | yes | Site slug, found in site settings. |
| `variables.title` | string | yes | Title shown for the pull request review. |
| `variables.sha` | string | yes | Current HEAD commit SHA of the branch being tested. |
| `variables.branch` | string | yes | Branch name being reviewed. |
| `variables.url` | string | yes | Preview deployment URL for the pull request review. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "startPullRequestReview": {
        "branch": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "markdownReport": "string",
        "metricBudgetStatus": "string",
        "sha": "string",
        "status": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `startPullRequestReview.branch` | string |  |
| `startPullRequestReview.createdAt` | date |  |
| `startPullRequestReview.markdownReport` | string |  |
| `startPullRequestReview.metricBudgetStatus` | string |  |
| `startPullRequestReview.sha` | string |  |
| `startPullRequestReview.status` | string |  |
| `startPullRequestReview.title` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pull-request-review.md) for the provider-specific parameters and requirements.

