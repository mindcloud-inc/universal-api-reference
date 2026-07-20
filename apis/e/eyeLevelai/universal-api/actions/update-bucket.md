# EyeLevel.ai: Update Bucket

Updates an existing bucket in EyeLevel.ai.

```
PUT https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/update-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EyeLevel.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/update-bucket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucketId": 1,
  "newName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/update-bucket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucketId": 1,
    "newName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucketId` | number | yes | The bucketId of the bucket being updated. |
| `newName` | string | yes | The new name of the bucket being renamed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucket": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucket` | object | The updated bucket. |

## Native endpoint

Through the native EyeLevel.ai API, this operation is `PUT /bucket/:bucketId` (base URL `https://api.groundx.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bucket.md) for the provider-specific parameters and requirements.

