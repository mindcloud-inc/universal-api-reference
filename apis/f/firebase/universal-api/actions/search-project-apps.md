# Firebase: Search Project Apps

Finds apps in a Firebase project.

```
GET https://connect.mindcloud.co/v1/universal/firebase/latest/actions/search-project-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/search-project-apps?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/search-project-apps?${params}`, {
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
| `projectId` | string | yes | Firebase project ID. |
| `filter` | string | no | Firebase app search filter. |
| `showDeleted` | boolean | no | Whether deleted apps should be included in results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKeyId": "string",
      "appId": "string",
      "displayName": "Ava Chen",
      "expireTime": "string",
      "name": "Ava Chen",
      "namespace": "Ava Chen",
      "platform": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyId` | string | Associated API key ID. |
| `appId` | string | Firebase App ID. |
| `displayName` | string | User-assigned display name. |
| `expireTime` | string | Time the app expires, when applicable. |
| `name` | string | Firebase App resource name. |
| `namespace` | string | Platform-specific app namespace. |
| `platform` | string | Firebase App platform. |
| `state` | string | Lifecycle state of the Firebase App. |

## Native endpoint

Through the native Firebase API, this operation is `GET /v1beta1/projects/[:projectId]:searchApps` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-project-apps.md) for the provider-specific parameters and requirements.

