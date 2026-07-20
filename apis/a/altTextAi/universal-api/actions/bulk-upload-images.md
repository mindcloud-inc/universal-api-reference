# AltText.Ai: Bulk Upload Images

Bulk uploads image URLs for alt text generation in AltText.Ai.

```
POST https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/bulk-upload-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AltText.Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/bulk-upload-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/bulk-upload-images', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Optional email address to receive bulk upload results. |
| `file` | file | yes | CSV file containing image URLs to upload for bulk processing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "rowErrors": [
        [
          "string"
        ]
      ],
      "rows": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `rowErrors` | array<array> |  |
| `rows` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native AltText.Ai API, this operation is `POST /images/bulk_create` (base URL `https://alttext.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-upload-images.md) for the provider-specific parameters and requirements.

