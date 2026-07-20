# Modusign: Create Embedded Draft

Creates a new embedded draft in Modusign.

```
POST https://connect.mindcloud.co/v1/universal/modusign/latest/actions/create-embedded-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modusign/latest/actions/create-embedded-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modusign/latest/actions/create-embedded-draft', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "brandId": "string",
      "embeddedUrl": "https://example.com",
      "expiry": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brandId` | string | The associated brand ID, if any. |
| `embeddedUrl` | string | The URL to open the embedded draft editor. |
| `expiry` | string | The ISO timestamp when the embedded draft URL expires. |
| `id` | string | The embedded draft document ID. |

## Native endpoint

Through the native Modusign API, this operation is `POST /embedded-drafts` (base URL `https://api.modusign.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-embedded-draft.md) for the provider-specific parameters and requirements.

