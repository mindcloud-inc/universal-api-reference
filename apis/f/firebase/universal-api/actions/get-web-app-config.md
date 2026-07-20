# Firebase: Get Web App Config

Retrieves web app config from Firebase.

```
GET https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-web-app-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-web-app-config?connectionId=$CONNECTION_ID&projectId=string&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-web-app-config?${params}`, {
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
      "apiKey": "string",
      "appId": "string",
      "authDomain": "string",
      "databaseURL": "https://example.com",
      "locationId": "string",
      "measurementId": "string",
      "messagingSenderId": "string",
      "projectId": "string",
      "projectNumber": "string",
      "realtimeDatabaseUrl": "https://example.com",
      "storageBucket": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string | Web API key. |
| `appId` | string | Firebase Web App ID. |
| `authDomain` | string | Firebase Auth domain. |
| `databaseURL` | string | Default Realtime Database URL. |
| `locationId` | string | Default resource location ID. |
| `measurementId` | string | Google Analytics measurement ID. |
| `messagingSenderId` | string | Firebase Cloud Messaging sender ID. |
| `projectId` | string | Firebase Project ID. |
| `projectNumber` | string | Google-assigned project number. |
| `realtimeDatabaseUrl` | string | Realtime Database URL. |
| `storageBucket` | string | Default Cloud Storage bucket. |
| `version` | string | Config version. |

## Native endpoint

Through the native Firebase API, this operation is `GET /v1beta1/projects/[:projectId]/webApps/[:appId]/config` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-web-app-config.md) for the provider-specific parameters and requirements.

