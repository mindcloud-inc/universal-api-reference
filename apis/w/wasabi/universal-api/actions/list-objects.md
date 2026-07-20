# Wasabi: List Objects

Retrieves objects from a specific bucket in Wasabi.

```
GET https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/list-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/list-objects?connectionId=$CONNECTION_ID&bucketName=mindcloud-wasabi-agent-20260422-1214" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucketName": "mindcloud-wasabi-agent-20260422-1214"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasabi/latest/actions/list-objects?${params}`, {
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
| `bucketName` | string | yes | Name of the bucket to list objects from. Example: `mindcloud-wasabi-agent-20260422-1214`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucketName": "Ava Chen",
      "eTag": "string",
      "key": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "size": 1,
      "storageClass": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucketName` | string | Bucket that contains the object. |
| `eTag` | string | Object entity tag. |
| `key` | string | Object key. |
| `lastModified` | date | Object last modified timestamp. |
| `size` | number | Object size in bytes. |
| `storageClass` | string | Object storage class. |

## Native endpoint

Through the native Wasabi API, this operation is `GET /:bucketName` (base URL `https://s3.wasabisys.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-objects.md) for the provider-specific parameters and requirements.

