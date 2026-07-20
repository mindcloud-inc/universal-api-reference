# Firebase: Create Android SHA Certificate

Creates an Android SHA certificate in Firebase.

```
POST https://connect.mindcloud.co/v1/universal/firebase/latest/actions/create-android-sha-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/create-android-sha-certificate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "appId": "string",
  "certType": "string",
  "shaHash": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebase/latest/actions/create-android-sha-certificate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "appId": "string",
    "certType": "string",
    "shaHash": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Firebase project ID. |
| `appId` | string | yes | Firebase Android app ID. |
| `certType` | string | yes | Type of SHA certificate encoded in the hash. |
| `shaHash` | string | yes | Certificate hash for the Android app. |

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

Through the native Firebase API, this operation is `POST /v1beta1/projects/[:projectId]/androidApps/[:appId]/sha` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-android-sha-certificate.md) for the provider-specific parameters and requirements.

