# Firebase: List Android SHA Certificates

Retrieves Android SHA certificates from Firebase.

```
GET https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-android-sha-certificates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-android-sha-certificates?connectionId=$CONNECTION_ID&projectId=string&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-android-sha-certificates?${params}`, {
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
| `appId` | string | yes | Firebase Android app ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certType": "string",
      "name": "Ava Chen",
      "shaHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certType` | string | SHA certificate type. |
| `name` | string | SHA certificate resource name. |
| `shaHash` | string | SHA certificate hash. |

## Native endpoint

Through the native Firebase API, this operation is `GET /v1beta1/projects/[:projectId]/androidApps/[:appId]/sha` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-android-sha-certificates.md) for the provider-specific parameters and requirements.

