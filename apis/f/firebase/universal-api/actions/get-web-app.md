# Firebase: Get Web App

Retrieves a web app from Firebase.

```
GET https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-web-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-web-app?connectionId=$CONNECTION_ID&projectId=string&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-web-app?${params}`, {
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
| `appId` | string | yes | Firebase Web app ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKeyId": "string",
      "appId": "string",
      "appUrls": [
        "https://example.com"
      ],
      "displayName": "Ava Chen",
      "etag": "string",
      "expireTime": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "state": "string",
      "webId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKeyId` | string | Associated API key ID. |
| `appId` | string | Firebase Web App ID. |
| `appUrls` | array<string> | Registered web app URLs. |
| `displayName` | string | User-assigned display name. |
| `etag` | string | Server-computed concurrency token. |
| `expireTime` | string | Time the app expires, when applicable. |
| `name` | string | Firebase Web App resource name. |
| `projectId` | string | Firebase Project ID. |
| `state` | string | Lifecycle state of the Web App. |
| `webId` | string | Web app ID used in Firebase config. |

## Native endpoint

Through the native Firebase API, this operation is `GET /v1beta1/projects/[:projectId]/webApps/[:appId]` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-web-app.md) for the provider-specific parameters and requirements.

