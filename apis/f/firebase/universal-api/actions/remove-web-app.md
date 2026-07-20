# Firebase: Remove Web App

Removes a web app from Firebase.

```
DELETE https://connect.mindcloud.co/v1/universal/firebase/latest/actions/remove-web-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/remove-web-app?connectionId=$CONNECTION_ID&projectId=string&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/remove-web-app?${params}`, {
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
| `allowMissing` | boolean | no | Allow the request to succeed when the app is already absent. |
| `validateOnly` | boolean | no | Validate the request without removing the web app. |
| `immediate` | boolean | no | Remove the app immediately instead of allowing the normal expiration window. |
| `etag` | string | no | Checksum used to avoid removing a stale web app resource. |

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

Through the native Firebase API, this operation is `POST /v1beta1/projects/[:projectId]/webApps/[:appId]:remove` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-web-app.md) for the provider-specific parameters and requirements.

