# Cloudmersive Security: Detect and Normalize XSS

Detects and normalizes XSS threats in Cloudmersive Security.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-and-normalize-xss
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Security `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-and-normalize-xss?connectionId=$CONNECTION_ID&inputText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-and-normalize-xss?${params}`, {
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
| `inputText` | string | yes | Text input to scan and normalize for cross-site scripting attacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ContainedXss": true,
      "NormalizedResult": "string",
      "OriginalInput": "string",
      "Successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ContainedXss` | boolean |  |
| `NormalizedResult` | string |  |
| `OriginalInput` | string |  |
| `Successful` | boolean |  |

## Native endpoint

Through the native Cloudmersive Security API, this operation is `POST /security/threat-detection/content/xss/detect/string` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-and-normalize-xss.md) for the provider-specific parameters and requirements.

