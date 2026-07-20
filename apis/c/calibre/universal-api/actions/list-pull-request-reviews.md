# Calibre: List Pull Request Reviews

Retrieves pull request reviews from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-pull-request-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-pull-request-reviews?connectionId=$CONNECTION_ID&variables.site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-pull-request-reviews?${params}`, {
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
| `variables.site` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organisation": {
        "site": {
          "pullRequestReviews": [
            {
              "branch": "string",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "markdownReport": "string",
              "sha": "string",
              "status": "string",
              "title": "string"
            }
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organisation.site.pullRequestReviews[].branch` | string |  |
| `organisation.site.pullRequestReviews[].createdAt` | date |  |
| `organisation.site.pullRequestReviews[].markdownReport` | string |  |
| `organisation.site.pullRequestReviews[].sha` | string |  |
| `organisation.site.pullRequestReviews[].status` | string |  |
| `organisation.site.pullRequestReviews[].title` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pull-request-reviews.md) for the provider-specific parameters and requirements.

