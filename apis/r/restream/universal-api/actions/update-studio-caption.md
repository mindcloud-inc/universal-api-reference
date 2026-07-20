# Restream: Update Studio Caption

Updates a studio caption in Restream.

```
PUT https://connect.mindcloud.co/v1/universal/restream/latest/actions/update-studio-caption
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/restream/latest/actions/update-studio-caption" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "captionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restream/latest/actions/update-studio-caption', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "captionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `captionId` | string | yes | The ID of the caption to update. |
| `secondaryText` | string | no | Updated caption secondary text. |
| `text` | string | no | Updated caption text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brandId": "string",
      "id": "string",
      "secondaryText": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brandId` | string |  |
| `id` | string |  |
| `secondaryText` | string |  |
| `text` | string |  |

## Native endpoint

Through the native Restream API, this operation is `PATCH /user/studio/captions/:captionId` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-studio-caption.md) for the provider-specific parameters and requirements.

