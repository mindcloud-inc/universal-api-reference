# Pirsonal: List Templates

Retrieves templates from your Pirsonal account.

```
GET https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pirsonal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/list-templates?${params}`, {
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
      "analytics": {},
      "date": "string",
      "description": "string",
      "id": "string",
      "inputMedias": [
        {}
      ],
      "inputScripts": [
        "string"
      ],
      "name": "Ava Chen",
      "outProfiles": [
        "string"
      ],
      "secret": "string",
      "status": "string",
      "template_type": "string",
      "videoInputs": {},
      "videoOutput": {},
      "videosCSV": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analytics` | object | Template analytics. |
| `date` | string | Template creation date. |
| `description` | string | Template description. |
| `id` | string | Template ID. |
| `inputMedias` | array<object> | Template input media definitions. |
| `inputScripts` | array<string> | Template input scripts. |
| `name` | string | Template name. |
| `outProfiles` | array<string> | Output profile names. |
| `secret` | string | Template secret. |
| `status` | string | Template status. |
| `template_type` | string | Template type. |
| `videoInputs` | object | Template video input counts. |
| `videoOutput` | object | Template video output settings. |
| `videosCSV` | number | Template CSV video count. |

## Native endpoint

Through the native Pirsonal API, this operation is `POST /api` (base URL `https://app.pirsonal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

