# Firebase: Get Firebase Project

Retrieves a Firebase project.

```
GET https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-firebase-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-firebase-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-firebase-project?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotations": {},
      "displayName": "Ava Chen",
      "etag": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "projectNumber": "string",
      "resources": {},
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotations` | object | User-defined project annotations. |
| `displayName` | string | User-assigned display name. |
| `etag` | string | Server-computed concurrency token. |
| `name` | string | Firebase Project resource name. |
| `projectId` | string | User-assigned unique project ID. |
| `projectNumber` | string | Google-assigned project number. |
| `resources` | object | Associated Google Cloud resources. |
| `state` | string | Lifecycle state of the Firebase Project. |

## Native endpoint

Through the native Firebase API, this operation is `GET /v1beta1/projects/[:projectId]` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-firebase-project.md) for the provider-specific parameters and requirements.

