# Power Assist: Slugify String

Converts a string into a slug with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/slugify-string
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/slugify-string?connectionId=$CONNECTION_ID&string=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "string": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/slugify-string?${params}`, {
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
| `string` | string | yes | The text to transform into a URL-safe slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | string | Slugified string result. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/string/slugify` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/slugify-string.md) for the provider-specific parameters and requirements.

