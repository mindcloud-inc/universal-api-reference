# Postmark: Validate Template

Validates a template in Postmark.

```
POST https://connect.mindcloud.co/v1/universal/postmark/latest/actions/validate-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/validate-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmark/latest/actions/validate-template', {
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
      "AllContentIsValid": true,
      "HtmlBody": {
        "ContentIsValid": true,
        "RenderedContent": "string",
        "ValidationErrors": [
          [
            {}
          ]
        ]
      },
      "Subject": {
        "ContentIsValid": true,
        "RenderedContent": "string",
        "ValidationErrors": [
          [
            {}
          ]
        ]
      },
      "SuggestedTemplateModel": {},
      "TextBody": {
        "ContentIsValid": true,
        "RenderedContent": "string",
        "ValidationErrors": [
          [
            {}
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AllContentIsValid` | boolean |  |
| `HtmlBody` | object |  |
| `HtmlBody.ContentIsValid` | boolean |  |
| `HtmlBody.RenderedContent` | string |  |
| `HtmlBody.ValidationErrors[]` | array<object> |  |
| `Subject` | object |  |
| `Subject.ContentIsValid` | boolean |  |
| `Subject.RenderedContent` | string |  |
| `Subject.ValidationErrors[]` | array<object> |  |
| `SuggestedTemplateModel` | object |  |
| `TextBody` | object |  |
| `TextBody.ContentIsValid` | boolean |  |
| `TextBody.RenderedContent` | string |  |
| `TextBody.ValidationErrors[]` | array<object> |  |

## Native endpoint

Through the native Postmark API, this operation is `POST /templates/validate` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-template.md) for the provider-specific parameters and requirements.

