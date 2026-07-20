# Firebase: Delete Android SHA Certificate

Deletes an Android SHA certificate from Firebase.

```
DELETE https://connect.mindcloud.co/v1/universal/firebase/latest/actions/delete-android-sha-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/delete-android-sha-certificate?connectionId=$CONNECTION_ID&projectId=string&appId=string&shaHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "appId": "string",
  "shaHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/delete-android-sha-certificate?${params}`, {
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
| `shaHash` | string | yes | SHA certificate hash. |

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

Through the native Firebase API, this operation is `DELETE /v1beta1/projects/[:projectId]/androidApps/[:appId]/sha/[:shaHash]` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-android-sha-certificate.md) for the provider-specific parameters and requirements.

