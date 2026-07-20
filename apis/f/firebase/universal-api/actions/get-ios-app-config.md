# Firebase: Get iOS App Config

Retrieves iOS app config from Firebase.

```
GET https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-ios-app-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-ios-app-config?connectionId=$CONNECTION_ID&projectId=string&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-ios-app-config?${params}`, {
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
| `appId` | string | yes | Firebase iOS app ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configFileContents": "string",
      "configFilename": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configFileContents` | string | Base64-encoded GoogleService-Info.plist contents. |
| `configFilename` | string | Suggested filename for the iOS app config file. |

## Native endpoint

Through the native Firebase API, this operation is `GET /v1beta1/projects/[:projectId]/iosApps/[:appId]/config` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ios-app-config.md) for the provider-specific parameters and requirements.

