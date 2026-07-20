# Firebase: Add Firebase To Project

Adds Firebase to a Google Cloud project.

```
POST https://connect.mindcloud.co/v1/universal/firebase/latest/actions/add-firebase-to-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/add-firebase-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebase/latest/actions/add-firebase-to-project', {
  method: 'POST',
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
| `projectId` | string | yes | Firebase or Google Cloud project ID. |
| `locationId` | string | no | Deprecated location ID from AddFirebaseRequest; may be ignored for newer projects. |

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

Through the native Firebase API, this operation is `POST /v1beta1/projects/[:projectId]:addFirebase` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-firebase-to-project.md) for the provider-specific parameters and requirements.

