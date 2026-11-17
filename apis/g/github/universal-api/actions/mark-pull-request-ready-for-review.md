# GitHub: Mark Pull Request Ready for Review



```
PUT https://connect.mindcloud.co/v1/universal/github/latest/actions/mark-pull-request-ready-for-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/github/latest/actions/mark-pull-request-ready-for-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pullRequestId": "PR_kwDOAbc123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/github/latest/actions/mark-pull-request-ready-for-review', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pullRequestId": "PR_kwDOAbc123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pullRequestId` | string | yes | The pull request's GraphQL node ID (node_id from the REST API). Example: `PR_kwDOAbc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "markPullRequestReadyForReview": {
          "pullRequest": {
            "isDraft": true,
            "number": 1
          }
        }
      },
      "errors": [
        {
          "message": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.markPullRequestReadyForReview.pullRequest.isDraft` | boolean |  |
| `data.markPullRequestReadyForReview.pullRequest.number` | number |  |
| `errors[].message` | string |  |
| `errors[].type` | string |  |

## Native endpoint

Through the native GitHub API, this operation is `POST /graphql` (base URL `https://api.github.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-pull-request-ready-for-review.md) for the provider-specific parameters and requirements.

