# LaunchDarkly: Get Project

Retrieves a project from LaunchDarkly.

```
GET https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchDarkly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-project?connectionId=$CONNECTION_ID&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/get-project?${params}`, {
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
| `projectKey` | string | yes | The LaunchDarkly project key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultClientSideAvailability": {},
      "id": "string",
      "includeInSnippetByDefault": true,
      "key": "string",
      "links": {},
      "name": "Ava Chen",
      "requireViewAssociationForNewFlags": true,
      "requireViewAssociationForNewSegments": true,
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultClientSideAvailability` | object |  |
| `id` | string |  |
| `includeInSnippetByDefault` | boolean |  |
| `key` | string |  |
| `links` | object |  |
| `name` | string |  |
| `requireViewAssociationForNewFlags` | boolean |  |
| `requireViewAssociationForNewSegments` | boolean |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native LaunchDarkly API, this operation is `GET /projects/:projectKey` (base URL `https://app.launchdarkly.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

