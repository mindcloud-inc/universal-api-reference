# Firebase: Remove Analytics From Project

Removes Google Analytics from a Firebase project.

```
DELETE https://connect.mindcloud.co/v1/universal/firebase/latest/actions/remove-analytics-from-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/remove-analytics-from-project?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/remove-analytics-from-project?${params}`, {
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
| `analyticsPropertyId` | string | no | Google Analytics property ID associated with the Firebase project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Connector success marker for Firebase empty responses; a successful HTTP status indicates completion. |

## Native endpoint

Through the native Firebase API, this operation is `POST /v1beta1/projects/[:projectId]:removeAnalytics` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-analytics-from-project.md) for the provider-specific parameters and requirements.

