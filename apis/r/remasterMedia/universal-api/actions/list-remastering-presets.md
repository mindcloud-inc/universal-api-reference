# RemasterMedia: List Remastering Presets

Retrieves remastering presets from RemasterMedia.

```
GET https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/list-remastering-presets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemasterMedia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/list-remastering-presets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/list-remastering-presets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {
          "presets": [
            {
              "definition_file": "string",
              "description": "string",
              "name": "Ava Chen",
              "title": "string",
              "updated_at": "2026-05-07T12:00:00.000Z"
            }
          ],
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> | Preset categories. |
| `categories[].presets` | array<object> |  |
| `categories[].presets[].definition_file` | string |  |
| `categories[].presets[].description` | string |  |
| `categories[].presets[].name` | string |  |
| `categories[].presets[].title` | string |  |
| `categories[].presets[].updated_at` | date |  |
| `categories[].title` | string |  |

## Native endpoint

Through the native RemasterMedia API, this operation is `GET /actions/remaster/presets` (base URL `https://api-sandbox.remastermedia.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-remastering-presets.md) for the provider-specific parameters and requirements.

