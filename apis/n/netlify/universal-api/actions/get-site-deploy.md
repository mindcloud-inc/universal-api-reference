# Netlify: Get Site Deploy



```
GET https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-site-deploy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-site-deploy?connectionId=$CONNECTION_ID&siteId=string&deployId=69aac8135e01826d281456d7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string",
  "deployId": "69aac8135e01826d281456d7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/get-site-deploy?${params}`, {
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
| `deployId` | string | yes | Example: `69aac8135e01826d281456d7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminUrl": "https://example.com",
      "agentRunnerId": "string",
      "availableFunctions": [
        {}
      ],
      "blobsRegion": "string",
      "branch": "string",
      "buildId": "string",
      "commitMessage": "string",
      "commitRef": "string",
      "committer": {},
      "commitUrl": "https://example.com",
      "context": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deploySslUrl": "https://example.com",
      "deployTime": 1,
      "deployUrl": "https://example.com",
      "deployValidationsReport": {},
      "edgeFunctionsPresent": true,
      "entryPath": "string",
      "errorMessage": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "framework": "string",
      "functionSchedules": [
        {}
      ],
      "id": "string",
      "lighthouse": {},
      "lighthousePluginScores": {},
      "links": {},
      "locked": true,
      "manualDeploy": true,
      "name": "Ava Chen",
      "pendingReviewReason": "string",
      "pluginState": "string",
      "publicRepo": true,
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "required": [
        "string"
      ],
      "requiredFunctions": [
        "string"
      ],
      "reviewId": "string",
      "reviewUrl": "https://example.com",
      "screenshotUrl": "https://example.com",
      "siteId": "string",
      "skewProtectionToken": "string",
      "skipped": true,
      "skippedLog": {},
      "sslUrl": "https://example.com",
      "state": "string",
      "strictContributorVerificationFailure": true,
      "summary": {},
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": "string",
      "viewsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminUrl` | string |  |
| `agentRunnerId` | string |  |
| `availableFunctions` | array<object> |  |
| `blobsRegion` | string |  |
| `branch` | string |  |
| `buildId` | string |  |
| `commitMessage` | string |  |
| `commitRef` | string |  |
| `committer` | object |  |
| `commitUrl` | string |  |
| `context` | string |  |
| `createdAt` | date |  |
| `deploySslUrl` | string |  |
| `deployTime` | number |  |
| `deployUrl` | string |  |
| `deployValidationsReport` | object |  |
| `edgeFunctionsPresent` | boolean |  |
| `entryPath` | string |  |
| `errorMessage` | string |  |
| `expiresAt` | date |  |
| `framework` | string |  |
| `functionSchedules` | array<object> |  |
| `id` | string |  |
| `lighthouse` | object |  |
| `lighthousePluginScores` | object |  |
| `links` | object |  |
| `locked` | boolean |  |
| `manualDeploy` | boolean |  |
| `name` | string |  |
| `pendingReviewReason` | string |  |
| `pluginState` | string |  |
| `publicRepo` | boolean |  |
| `publishedAt` | date |  |
| `required` | array<string> |  |
| `requiredFunctions` | array<string> |  |
| `reviewId` | string |  |
| `reviewUrl` | string |  |
| `screenshotUrl` | string |  |
| `siteId` | string |  |
| `skewProtectionToken` | string |  |
| `skipped` | boolean |  |
| `skippedLog` | object |  |
| `sslUrl` | string |  |
| `state` | string |  |
| `strictContributorVerificationFailure` | boolean |  |
| `summary` | object |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userId` | string |  |
| `viewsCount` | number |  |

## Native endpoint

Through the native Netlify API, this operation is `GET /sites/:site_id/deploys/:deploy_id` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-deploy.md) for the provider-specific parameters and requirements.

