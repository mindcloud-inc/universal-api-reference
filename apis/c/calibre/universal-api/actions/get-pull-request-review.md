# Calibre: Get Pull Request Review

Retrieves a pull request review by branch from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/get-pull-request-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/get-pull-request-review?connectionId=$CONNECTION_ID&variables.site=string&variables.branch=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.site": "string",
  "variables.branch": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/get-pull-request-review?${params}`, {
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
| `variables.branch` | string | yes |  |

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

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pull-request-review.md) for the provider-specific parameters and requirements.

