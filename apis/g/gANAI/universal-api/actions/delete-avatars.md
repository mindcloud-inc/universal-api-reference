# GAN.AI: Delete Avatars

Deletes avatars in bulk from GAN.AI.

```
DELETE https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/delete-avatars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/delete-avatars?connectionId=$CONNECTION_ID&avatarIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "avatarIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/delete-avatars?${params}`, {
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
| `avatarIds[]` | array<string> | yes | List of avatar IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associatedInferencesDeletedCount": 1,
      "deletedAvatarIds": [
        "string"
      ],
      "deletedAvatarsCount": 1,
      "deletionFailedAvatarsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associatedInferencesDeletedCount` | number |  |
| `deletedAvatarIds[]` | string |  |
| `deletedAvatarsCount` | number |  |
| `deletionFailedAvatarsCount` | number |  |

## Native endpoint

Through the native GAN.AI API, this operation is `DELETE /v1/avatars/bulk_delete_avatars` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-avatars.md) for the provider-specific parameters and requirements.

