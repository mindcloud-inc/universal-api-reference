# Firebase: Get Admin SDK Config

Retrieves Admin SDK config for a Firebase project.

```
GET https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-admin-sdk-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-admin-sdk-config?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-admin-sdk-config?${params}`, {
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
      "databaseURL": "https://example.com",
      "locationId": "string",
      "projectId": "string",
      "storageBucket": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `databaseURL` | string | Default Realtime Database URL. |
| `locationId` | string | Default resource location ID. |
| `projectId` | string | Firebase Project ID. |
| `storageBucket` | string | Default Cloud Storage bucket. |

## Native endpoint

Through the native Firebase API, this operation is `GET /v1beta1/projects/[:projectId]/adminSdkConfig` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-admin-sdk-config.md) for the provider-specific parameters and requirements.

