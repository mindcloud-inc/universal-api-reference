# Netlify: List Site Builds



```
GET https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-site-builds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-site-builds?connectionId=$CONNECTION_ID&limit=25&offset=0&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-site-builds?${params}`, {
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
| `siteId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deployId": "string",
      "deployPendingReviewReason": "string",
      "deployState": "string",
      "done": true,
      "error": "string",
      "id": "string",
      "sha": "string",
      "strictContributorVerificationFailure": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `deployId` | string |  |
| `deployPendingReviewReason` | string |  |
| `deployState` | string |  |
| `done` | boolean |  |
| `error` | string |  |
| `id` | string |  |
| `sha` | string |  |
| `strictContributorVerificationFailure` | boolean |  |

## Native endpoint

Through the native Netlify API, this operation is `GET /sites/:site_id/builds` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-site-builds.md) for the provider-specific parameters and requirements.

