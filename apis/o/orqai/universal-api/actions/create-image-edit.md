# Orq.ai: Create Image Edit

Creates an image edit in Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-image-edit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-image-edit?connectionId=$CONNECTION_ID&image=string&model=string&prompt=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "image": "string",
  "model": "string",
  "prompt": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-image-edit?${params}`, {
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
| `image` | file | yes |  |
| `model` | string | yes |  |
| `prompt` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "data": [
        {
          "url": "https://example.com"
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
| `created` | number |  |
| `data[].url` | string |  |

## Native endpoint

Through the native Orq.ai API, this operation is `POST /v2/router/images/edits` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image-edit.md) for the provider-specific parameters and requirements.

