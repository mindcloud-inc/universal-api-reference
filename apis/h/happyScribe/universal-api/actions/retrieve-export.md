# HappyScribe: Retrieve Export

Retrieves an export from HappyScribe.

```
GET https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/retrieve-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyScribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/retrieve-export?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/retrieve-export?${params}`, {
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
| `id` | string | yes | The export identifier. |

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

Through the native HappyScribe API, this operation is `GET /exports/:id` (base URL `https://www.happyscribe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-export.md) for the provider-specific parameters and requirements.

