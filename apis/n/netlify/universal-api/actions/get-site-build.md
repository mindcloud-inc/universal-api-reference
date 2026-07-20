# Netlify: Get Site Build



```
GET https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-site-build
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-site-build?connectionId=$CONNECTION_ID&buildId=69aac8135e01826d281456d5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "buildId": "69aac8135e01826d281456d5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-site-build?${params}`, {
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
| `buildId` | string | yes | Example: `69aac8135e01826d281456d5`. |

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

Through the native Netlify API, this operation is `GET /builds/:build_id` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-build.md) for the provider-specific parameters and requirements.

