# Firebase: Update Firebase Project

Updates an existing Firebase project.

```
PUT https://connect.mindcloud.co/v1/universal/firebase/latest/actions/update-firebase-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/update-firebase-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebase/latest/actions/update-firebase-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Firebase project ID. |
| `updateMask` | string | no | Comma-separated FirebaseProject fields to update. |
| `displayName` | string | no | User-assigned Firebase project display name. |
| `etag` | string | no | Checksum used to avoid overwriting stale project data. |

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

Through the native Firebase API, this operation is `PATCH /v1beta1/projects/[:projectId]` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-firebase-project.md) for the provider-specific parameters and requirements.

