# Apify: List Actor Versions

Retrieves actor versions for an Apify actor.

```
GET https://connect.mindcloud.co/v1/universal/apify/latest/actions/list-actor-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apify/latest/actions/list-actor-versions?connectionId=$CONNECTION_ID&actorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apify/latest/actions/list-actor-versions?${params}`, {
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
| `actorId` | string | yes | The ID or username of the actor whose versions to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applyEnvVarsToBuild": true,
      "buildTag": "string",
      "gitRepoUrl": "https://example.com",
      "sourceType": "string",
      "versionNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applyEnvVarsToBuild` | boolean |  |
| `buildTag` | string |  |
| `gitRepoUrl` | string |  |
| `sourceType` | string |  |
| `versionNumber` | string |  |

## Native endpoint

Through the native Apify API, this operation is `GET /v2/acts/:actorId/versions` (base URL `https://api.apify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-actor-versions.md) for the provider-specific parameters and requirements.

