# Autype: Validate Markdown

Validates document markdown content in Autype.

```
GET https://connect.mindcloud.co/v1/universal/autype/latest/actions/validate-markdown
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/validate-markdown?connectionId=$CONNECTION_ID&content=string&document=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "content": "string",
  "document": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autype/latest/actions/validate-markdown?${params}`, {
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
| `content` | string | yes |  |
| `document` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {
          "code": "string",
          "message": "string",
          "path": "string"
        }
      ],
      "valid": true,
      "warnings": [
        {
          "code": "string",
          "message": "string",
          "path": "string"
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
| `errors[].code` | string |  |
| `errors[].message` | string |  |
| `errors[].path` | string |  |
| `valid` | boolean |  |
| `warnings[].code` | string |  |
| `warnings[].message` | string |  |
| `warnings[].path` | string |  |

## Native endpoint

Through the native Autype API, this operation is `POST /render/validate/markdown` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-markdown.md) for the provider-specific parameters and requirements.

