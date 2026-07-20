# Google Cloud Storage: Restore Object

Restores a soft-deleted object in Google Cloud Storage.

```
POST https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/restore-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/restore-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucket": "string",
  "object": "string",
  "generation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/restore-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucket": "string",
    "object": "string",
    "generation": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucket` | list<string> | yes | Bucket containing the soft-deleted object. |
| `object` | string | yes | Soft-deleted object name. |
| `generation` | string | yes | Generation of the soft-deleted object to restore. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucket": "string",
      "generation": "string",
      "id": "string",
      "name": "Ava Chen",
      "restoreToken": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucket` | string |  |
| `generation` | string |  |
| `id` | string |  |
| `name` | string |  |
| `restoreToken` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Google Cloud Storage API, this operation is `POST /storage/v1/b/:bucket/o/:object/restore` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-object.md) for the provider-specific parameters and requirements.

