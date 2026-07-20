# Firebase: List iOS Apps

Retrieves iOS apps from Firebase.

```
GET https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-ios-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-ios-apps?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-ios-apps?${params}`, {
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
| `showDeleted` | string | no | Whether deleted iOS apps should be included in results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKeyId": "string",
      "appId": "string",
      "appStoreId": "string",
      "bundleId": "string",
      "displayName": "Ava Chen",
      "etag": "string",
      "expireTime": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "state": "string",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyId` | string | Associated API key ID. |
| `appId` | string | Firebase iOS App ID. |
| `appStoreId` | string | Apple App Store ID. |
| `bundleId` | string | Apple bundle ID. |
| `displayName` | string | User-assigned display name. |
| `etag` | string | Server-computed concurrency token. |
| `expireTime` | string | Time the app expires, when applicable. |
| `name` | string | Firebase iOS App resource name. |
| `projectId` | string | Firebase Project ID. |
| `state` | string | Lifecycle state of the iOS App. |
| `teamId` | string | Apple Developer Team ID. |

## Native endpoint

Through the native Firebase API, this operation is `GET /v1beta1/projects/[:projectId]/iosApps` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ios-apps.md) for the provider-specific parameters and requirements.

