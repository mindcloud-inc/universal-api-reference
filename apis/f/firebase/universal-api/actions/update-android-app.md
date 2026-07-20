# Firebase: Update Android App

Updates an existing Android app in Firebase.

```
PUT https://connect.mindcloud.co/v1/universal/firebase/latest/actions/update-android-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/update-android-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "appId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebase/latest/actions/update-android-app', {
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
| `appId` | string | yes | Firebase Android app ID. |
| `updateMask` | string | no | Comma-separated field mask specifying which Android app fields to update. |
| `displayName` | string | no | User-assigned display name for the Android app. |
| `apiKeyId` | string | no | Google-assigned UID for the Firebase API key associated with the Android app. |
| `etag` | string | no | Checksum sent with update requests to avoid overwriting a stale Android app resource. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKeyId": "string",
      "appId": "string",
      "displayName": "Ava Chen",
      "etag": "string",
      "expireTime": "string",
      "name": "Ava Chen",
      "packageName": "Ava Chen",
      "projectId": "string",
      "sha1Hashes": [
        "string"
      ],
      "sha256Hashes": [
        "string"
      ],
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
| `appId` | string | Firebase Android App ID. |
| `displayName` | string | User-assigned display name. |
| `etag` | string | Server-computed concurrency token. |
| `expireTime` | string | Time the app expires, when applicable. |
| `name` | string | Firebase Android App resource name. |
| `packageName` | string | Android package name. |
| `projectId` | string | Firebase Project ID. |
| `sha1Hashes` | array<string> | Registered SHA-1 certificate hashes. |
| `sha256Hashes` | array<string> | Registered SHA-256 certificate hashes. |
| `state` | string | Lifecycle state of the Android App. |

## Native endpoint

Through the native Firebase API, this operation is `PATCH /v1beta1/projects/[:projectId]/androidApps/[:appId]` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-android-app.md) for the provider-specific parameters and requirements.

