# Apify: Get Actor

Retrieves an actor from Apify.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor?connectionId=$CONNECTION_ID&actorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor?${params}`, {
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
| `actorId` | string | yes | The ID or username of the actor to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "actorPermissionLevel": "string",
        "categories": [
          "string"
        ],
        "createdAt": "2026-05-07T12:00:00.000Z",
        "defaultRunOptions": {
          "build": "string",
          "memoryMbytes": 1,
          "timeoutSecs": 1
        },
        "deploymentKey": "string",
        "description": "string",
        "exampleRunInput": {
          "body": "string",
          "contentType": "string"
        },
        "hasNoDataset": true,
        "id": "string",
        "isCritical": true,
        "isDeprecated": true,
        "isGeneric": true,
        "isPublic": true,
        "isSourceCodeHidden": true,
        "modifiedAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "notice": "string",
        "pictureUrl": "https://example.com",
        "seoDescription": {},
        "seoTitle": "string",
        "standbyUrl": {},
        "stats": {
          "actorReviewCount": 1,
          "actorReviewRating": 1,
          "bookmarkCount": 1,
          "lastRunStartedAt": "2026-05-07T12:00:00.000Z",
          "publicActorRunStats30Days": {
            "aborted": 1,
            "failed": 1,
            "succeeded": 1,
            "total": 1
          },
          "totalBuilds": 1,
          "totalMetamorphs": 1,
          "totalRuns": 1,
          "totalUsers": 1,
          "totalUsers30Days": 1,
          "totalUsers7Days": 1,
          "totalUsers90Days": 1
        },
        "taggedBuilds": {
          "latest": {
            "buildId": "string",
            "buildNumber": "string",
            "buildNumberInt": 1,
            "finishedAt": "2026-05-07T12:00:00.000Z"
          }
        },
        "title": "string",
        "userId": "string",
        "username": "Ava Chen",
        "versions": [
          {
            "buildTag": "string",
            "gitRepoUrl": "https://example.com",
            "sourceFiles": [
              {
                "content": "string",
                "format": "string",
                "name": "Ava Chen"
              }
            ],
            "sourceType": "string",
            "versionNumber": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.actorPermissionLevel` | string |  |
| `data.categories[]` | string |  |
| `data.createdAt` | date |  |
| `data.defaultRunOptions.build` | string |  |
| `data.defaultRunOptions.memoryMbytes` | number |  |
| `data.defaultRunOptions.timeoutSecs` | number |  |
| `data.deploymentKey` | string |  |
| `data.description` | string |  |
| `data.exampleRunInput.body` | string |  |
| `data.exampleRunInput.contentType` | string |  |
| `data.hasNoDataset` | boolean |  |
| `data.id` | string |  |
| `data.isCritical` | boolean |  |
| `data.isDeprecated` | boolean |  |
| `data.isGeneric` | boolean |  |
| `data.isPublic` | boolean |  |
| `data.isSourceCodeHidden` | boolean |  |
| `data.modifiedAt` | date |  |
| `data.name` | string |  |
| `data.notice` | string |  |
| `data.pictureUrl` | string |  |
| `data.seoDescription` | object |  |
| `data.seoTitle` | string |  |
| `data.standbyUrl` | object |  |
| `data.stats.actorReviewCount` | number |  |
| `data.stats.actorReviewRating` | number |  |
| `data.stats.bookmarkCount` | number |  |
| `data.stats.lastRunStartedAt` | date |  |
| `data.stats.publicActorRunStats30Days.aborted` | number |  |
| `data.stats.publicActorRunStats30Days.failed` | number |  |
| `data.stats.publicActorRunStats30Days.succeeded` | number |  |
| `data.stats.publicActorRunStats30Days.total` | number |  |
| `data.stats.totalBuilds` | number |  |
| `data.stats.totalMetamorphs` | number |  |
| `data.stats.totalRuns` | number |  |
| `data.stats.totalUsers` | number |  |
| `data.stats.totalUsers30Days` | number |  |
| `data.stats.totalUsers7Days` | number |  |
| `data.stats.totalUsers90Days` | number |  |
| `data.taggedBuilds.latest.buildId` | string |  |
| `data.taggedBuilds.latest.buildNumber` | string |  |
| `data.taggedBuilds.latest.buildNumberInt` | number |  |
| `data.taggedBuilds.latest.finishedAt` | date |  |
| `data.title` | string |  |
| `data.userId` | string |  |
| `data.username` | string |  |
| `data.versions[].buildTag` | string |  |
| `data.versions[].gitRepoUrl` | string |  |
| `data.versions[].sourceFiles[].content` | string |  |
| `data.versions[].sourceFiles[].format` | string |  |
| `data.versions[].sourceFiles[].name` | string |  |
| `data.versions[].sourceType` | string |  |
| `data.versions[].versionNumber` | string |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/acts/:actorId` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-actor.md) for the provider-specific parameters and requirements.

