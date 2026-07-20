# HappyScribe: Create Export

Creates a new export in HappyScribe.

```
POST https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/create-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyScribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/create-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "format": "txt",
  "transcriptionIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/create-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "format": "txt",
    "transcriptionIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | yes | Export format such as txt, docx, pdf, srt, vtt, json, or fcp. Example: `txt`. |
| `transcriptionIds[]` | array<string> | yes | One or more transcription IDs to export. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_link": "https://example.com",
      "format": "string",
      "id": "string",
      "state": "string",
      "transcription_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_link` | string |  |
| `format` | string |  |
| `id` | string |  |
| `state` | string |  |
| `transcription_ids` | array<string> |  |

## Native endpoint

Through the native HappyScribe API, this operation is `POST /exports` (base URL `https://www.happyscribe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-export.md) for the provider-specific parameters and requirements.

