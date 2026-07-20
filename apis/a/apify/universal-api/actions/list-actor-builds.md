# Apify: List Actor Builds

Retrieves actor builds for an Apify actor.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/list-actor-builds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/list-actor-builds?connectionId=$CONNECTION_ID&actorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/list-actor-builds?${params}`, {
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
| `actorId` | string | yes | The ID or username of the actor whose builds to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actId": "string",
      "buildNumber": "string",
      "buildNumberInt": 1,
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "meta": {
        "origin": "string"
      },
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "usageTotalUsd": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actId` | string |  |
| `buildNumber` | string |  |
| `buildNumberInt` | number |  |
| `finishedAt` | date |  |
| `id` | string |  |
| `meta.origin` | string |  |
| `startedAt` | date |  |
| `status` | string |  |
| `usageTotalUsd` | number |  |
| `userId` | string |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/acts/:actorId/builds` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-actor-builds.md) for the provider-specific parameters and requirements.

