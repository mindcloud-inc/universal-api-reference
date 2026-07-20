# Netlify: Create Site Deploy



```
POST https://connect.mindcloud.co/v1/universal/netlify/latest/actions/create-site-deploy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/create-site-deploy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netlify/latest/actions/create-site-deploy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | list<string> | yes |  |
| `deployPreviews` | boolean | no |  |
| `production` | boolean | no |  |
| `state` | list<string> | no | One of: `accepted`, `building`, `enqueued`, `error`, `new`, `pending_review`, `prepared`, `preparing`, `processed`, `processing`, `ready`, `rejected`, `retrying`, `uploaded`, `uploading`. |
| `branch` | string | no | Example: `main`. |
| `latestPublished` | boolean | no |  |
| `title` | string | no | Example: `Release deploy`. |
| `files` | object | no | A hash mapping file paths to SHA1 digests. |
| `zip` | file | no | Zip file content for the deploy payload. |
| `draft` | boolean | no |  |
| `async` | boolean | no |  |
| `functions` | object | no |  |
| `functionSchedules[]` | array<object> | no |  |
| `functionsConfig` | object | no |  |
| `framework` | string | no | Example: `astro`. |
| `frameworkVersion` | string | no | Example: `5.14.0`. |
| `environment[]` | array<object> | no | Deploy-specific environment variable data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deployUrl": "https://example.com",
      "id": "string",
      "manualDeploy": true,
      "name": "Ava Chen",
      "siteId": "string",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | string | Deploy context |
| `createdAt` | date | Creation timestamp |
| `deployUrl` | string | Deploy URL |
| `id` | string | Deploy ID |
| `manualDeploy` | boolean | Whether the deploy was created manually |
| `name` | string | Deploy name |
| `siteId` | string | Site ID |
| `state` | string | Deploy state |
| `updatedAt` | date | Last update timestamp |
| `url` | string | Published URL |

## Native endpoint

Through the native Netlify API, this operation is `POST /sites/:site_id/deploys` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site-deploy.md) for the provider-specific parameters and requirements.

