# Firebase: Create Android App

Creates an Android app in Firebase.

```
POST https://connect.mindcloud.co/v1/universal/firebase/latest/actions/create-android-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/create-android-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "packageName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebase/latest/actions/create-android-app', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "packageName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Firebase project ID. |
| `packageName` | string | yes | Canonical package name of the Android app. |
| `displayName` | string | no | User-assigned display name for the Android app. |
| `apiKeyId` | string | no | Google-assigned UID for the Firebase API key associated with the Android app. |
| `sha1Hashes[]` | array<string> | no | SHA-1 certificate hashes for the Android app. |
| `sha256Hashes[]` | array<string> | no | SHA-256 certificate hashes for the Android app. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "error": {},
      "metadata": {},
      "name": "Ava Chen",
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean | Whether the long-running operation is complete. |
| `error` | object | Operation error details, when present. |
| `metadata` | object | Service-specific operation metadata. |
| `name` | string | Server-assigned operation name. |
| `response` | object | Service-specific operation response. |

## Native endpoint

Through the native Firebase API, this operation is `POST /v1beta1/projects/[:projectId]/androidApps` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-android-app.md) for the provider-specific parameters and requirements.

