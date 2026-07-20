# EyeLevel.ai: Remove Bucket From Group

Removes a bucket from a group in EyeLevel.ai.

```
DELETE https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/remove-bucket-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EyeLevel.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/remove-bucket-from-group?connectionId=$CONNECTION_ID&groupId=1&bucketId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "1",
  "bucketId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/remove-bucket-from-group?${params}`, {
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
| `groupId` | number | yes | The groupId of the group that currently contains the bucket. |
| `bucketId` | number | yes | The bucketId of the bucket to remove from the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Association removal result message. |

## Native endpoint

Through the native EyeLevel.ai API, this operation is `DELETE /group/:groupId/bucket/:bucketId` (base URL `https://api.groundx.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-bucket-from-group.md) for the provider-specific parameters and requirements.

