# Firebase: Update iOS App

Updates an existing iOS app in Firebase.

```
PUT https://connect.mindcloud.co/v1/universal/firebase/latest/actions/update-ios-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/update-ios-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "appId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebase/latest/actions/update-ios-app', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "appId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Firebase project ID. |
| `appId` | string | yes | Firebase iOS app ID. |
| `updateMask` | string | no | Comma-separated field mask specifying which iOS app fields to update. |
| `displayName` | string | no | User-assigned display name for the iOS app. |
| `apiKeyId` | string | no | Google-assigned UID for the Firebase API key associated with the iOS app. |
| `appStoreId` | string | no | Apple ID assigned to the iOS app by the App Store. |
| `teamId` | string | no | Apple Developer Team ID associated with the app. |
| `etag` | string | no | Checksum sent with update requests to avoid overwriting a stale iOS app resource. |

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

Through the native Firebase API, this operation is `PATCH /v1beta1/projects/[:projectId]/iosApps/[:appId]` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ios-app.md) for the provider-specific parameters and requirements.

