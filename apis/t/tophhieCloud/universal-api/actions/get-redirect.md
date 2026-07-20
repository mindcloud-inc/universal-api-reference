# Tophhie Cloud: Get Redirect



```
GET https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-redirect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tophhie Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-redirect?connectionId=$CONNECTION_ID&application=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "application": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-redirect?${params}`, {
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
| `application` | string | yes | Application redirect key. Use index to fetch the redirect index. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        {}
      ],
      "links_count": 1,
      "root_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | array<object> | Redirect link rows. |
| `links_count` | number | Number of redirect links. |
| `root_url` | string | Root shortlink URL. |

## Native endpoint

Through the native Tophhie Cloud API, this operation is `GET /redirect/{application}` (base URL `https://api.tophhie.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-redirect.md) for the provider-specific parameters and requirements.

