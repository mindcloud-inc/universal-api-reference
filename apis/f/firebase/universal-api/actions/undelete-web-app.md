# Firebase: Undelete Web App

Restores a removed web app in Firebase.

```
PUT https://connect.mindcloud.co/v1/universal/firebase/latest/actions/undelete-web-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/undelete-web-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "appId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebase/latest/actions/undelete-web-app', {
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
| `appId` | string | yes | Firebase Web app ID. |
| `validateOnly` | boolean | no | Validate the request without restoring the web app. |
| `etag` | string | no | Checksum used to avoid restoring a stale web app resource. |

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

Through the native Firebase API, this operation is `POST /v1beta1/projects/[:projectId]/webApps/[:appId]:undelete` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/undelete-web-app.md) for the provider-specific parameters and requirements.

