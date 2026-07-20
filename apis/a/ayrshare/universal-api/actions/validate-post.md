# Ayrshare: Validate Post

Validates a post before publishing in Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/validate-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/validate-post?connectionId=$CONNECTION_ID&post=string&platforms%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "post": "string",
  "platforms[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/validate-post?${params}`, {
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
| `post` | string | yes | Post text to validate before publishing. |
| `platforms[]` | array<string> | yes | Platforms to validate the post against. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "errors": [
        {}
      ],
      "message": "string",
      "status": "string",
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Ayrshare error code. |
| `errors` | array<object> | Validation errors. |
| `message` | string | Validation or error message. |
| `status` | string | Validation status. |
| `warnings` | array<object> | Validation warnings. |

## Native endpoint

Through the native Ayrshare API, this operation is `POST /validate/post` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-post.md) for the provider-specific parameters and requirements.

