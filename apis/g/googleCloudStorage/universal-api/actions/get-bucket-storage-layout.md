# Google Cloud Storage: Get Bucket Storage Layout

Retrieves a bucket's storage layout from Google Cloud Storage.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/get-bucket-storage-layout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/get-bucket-storage-layout?connectionId=$CONNECTION_ID&bucket=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucket": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/get-bucket-storage-layout?${params}`, {
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
| `bucket` | list<string> | yes | Bucket name. |
| `prefix` | string | no | Object-name prefix for storage layout evaluation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucket": "string",
      "customPlacementConfig": {},
      "hierarchicalNamespace": {},
      "location": "string",
      "locationType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucket` | string |  |
| `customPlacementConfig` | object |  |
| `hierarchicalNamespace` | object |  |
| `location` | string |  |
| `locationType` | string |  |

## Native endpoint

Through the native Google Cloud Storage API, this operation is `GET /storage/v1/b/:bucket/storageLayout` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bucket-storage-layout.md) for the provider-specific parameters and requirements.

