# Apify: Get Actor Build

Retrieves an actor build from Apify.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor-build
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor-build?connectionId=$CONNECTION_ID&actorId=string&buildId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actorId": "string",
  "buildId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/get-actor-build?${params}`, {
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
| `actorId` | string | yes | The ID or username of the actor that owns the build. |
| `buildId` | string | yes | The ID of the build to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "actId": "string",
        "actorDefinition": {
          "input": {
            "properties": {
              "htmlString": {
                "description": "string",
                "editor": "string",
                "title": "string",
                "type": "string"
              }
            },
            "schemaVersion": 1,
            "title": "string",
            "type": "string"
          },
          "readme": "string"
        },
        "actVersion": {
          "buildTag": "string",
          "gitRepoUrl": "https://example.com",
          "sourceType": "string",
          "versionNumber": "string"
        },
        "buildNumber": "string",
        "finishedAt": "2026-05-07T12:00:00.000Z",
        "gitCommitId": "string",
        "id": "string",
        "inputSchema": "string",
        "meta": {
          "origin": "string"
        },
        "options": {
          "betaPackages": true,
          "diskMbytes": 1,
          "memoryMbytes": 1,
          "useCache": true
        },
        "readme": "string",
        "startedAt": "2026-05-07T12:00:00.000Z",
        "stats": {
          "computeUnits": 1,
          "durationMillis": 1,
          "imageSizeBytes": 1,
          "runTimeSecs": 1
        },
        "status": "string",
        "usageTotalUsd": 1,
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.actId` | string |  |
| `data.actorDefinition.input.properties.htmlString.description` | string |  |
| `data.actorDefinition.input.properties.htmlString.editor` | string |  |
| `data.actorDefinition.input.properties.htmlString.title` | string |  |
| `data.actorDefinition.input.properties.htmlString.type` | string |  |
| `data.actorDefinition.input.schemaVersion` | number |  |
| `data.actorDefinition.input.title` | string |  |
| `data.actorDefinition.input.type` | string |  |
| `data.actorDefinition.readme` | string |  |
| `data.actVersion.buildTag` | string |  |
| `data.actVersion.gitRepoUrl` | string |  |
| `data.actVersion.sourceType` | string |  |
| `data.actVersion.versionNumber` | string |  |
| `data.buildNumber` | string |  |
| `data.finishedAt` | date |  |
| `data.gitCommitId` | string |  |
| `data.id` | string |  |
| `data.inputSchema` | string |  |
| `data.meta.origin` | string |  |
| `data.options.betaPackages` | boolean |  |
| `data.options.diskMbytes` | number |  |
| `data.options.memoryMbytes` | number |  |
| `data.options.useCache` | boolean |  |
| `data.readme` | string |  |
| `data.startedAt` | date |  |
| `data.stats.computeUnits` | number |  |
| `data.stats.durationMillis` | number |  |
| `data.stats.imageSizeBytes` | number |  |
| `data.stats.runTimeSecs` | number |  |
| `data.status` | string |  |
| `data.usageTotalUsd` | number |  |
| `data.userId` | string |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/acts/:actorId/builds/:buildId` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-actor-build.md) for the provider-specific parameters and requirements.

