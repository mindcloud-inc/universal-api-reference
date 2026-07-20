# GAN.AI: Delete Avatar Videos Bulk

Deletes avatar videos in bulk from GAN.AI.

```
DELETE https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/delete-avatar-videos-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/delete-avatar-videos-bulk?connectionId=$CONNECTION_ID&inferenceIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inferenceIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/delete-avatar-videos-bulk?${params}`, {
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
| `inferenceIds[]` | array<string> | yes | List of avatar inference IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedInferenceIds": [
        "string"
      ],
      "deletedInferencesCount": 1,
      "deletionFailedInferencesCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedInferenceIds[]` | string |  |
| `deletedInferencesCount` | number |  |
| `deletionFailedInferencesCount` | number |  |

## Native endpoint

Through the native GAN.AI API, this operation is `DELETE /v1/avatars/bulk_delete_avatar_inferences` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-avatar-videos-bulk.md) for the provider-specific parameters and requirements.

