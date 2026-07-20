# DigiParser: Upload via URL



```
POST https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/upload-via-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/upload-via-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parserId": "string",
  "urls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digiParser/latest/actions/upload-via-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parserId": "string",
    "urls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parserId` | string | yes | Parser UUID from DigiParser Parser Settings -> General Settings. |
| `urls[]` | array<string> | yes | URLs pointing to document files, up to 20 per request. |
| `folderId` | string | no | Optional folder UUID to assign created documents to that folder. |
| `externalIds[]` | array<string> | no | Optional array of external IDs, one per URL. |
| `custom[]` | array<object> | no | Optional array of tracking objects, one per URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<object> | Created document rows with IDs, URLs, processing status, and operation metadata. |
| `success` | boolean | Whether the upload request was accepted. |

## Native endpoint

Through the native DigiParser API, this operation is `POST /api/v1/process/:parserId/urls` (base URL `https://app.digiparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-via-url.md) for the provider-specific parameters and requirements.

