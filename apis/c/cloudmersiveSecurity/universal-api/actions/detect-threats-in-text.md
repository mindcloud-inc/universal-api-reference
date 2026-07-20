# Cloudmersive Security: Detect Threats in Text

Detects threats in text with Cloudmersive Security.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-threats-in-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Security `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-threats-in-text?connectionId=$CONNECTION_ID&inputText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-threats-in-text?${params}`, {
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
| `inputText` | string | yes | User-facing text input to scan for SQLI, XSS, XXE, SSRF, and JSON insecure deserialization threats. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CleanResult": true,
      "ContainedJsonInsecureDeserializationAttack": true,
      "ContainedSqlInjectionThreat": true,
      "ContainedSsrfThreat": true,
      "ContainedXssThreat": true,
      "ContainedXxeThreat": true,
      "IsJSON": true,
      "IsURL": true,
      "IsXML": true,
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
| `CleanResult` | boolean | True when the input did not contain detected threats. |
| `ContainedJsonInsecureDeserializationAttack` | boolean |  |
| `ContainedSqlInjectionThreat` | boolean |  |
| `ContainedSsrfThreat` | boolean |  |
| `ContainedXssThreat` | boolean |  |
| `ContainedXxeThreat` | boolean |  |
| `IsJSON` | boolean |  |
| `IsURL` | boolean |  |
| `IsXML` | boolean |  |
| `OriginalInput` | string |  |
| `Successful` | boolean | True if the operation was successful. |

## Native endpoint

Through the native Cloudmersive Security API, this operation is `POST /security/threat-detection/content/automatic/detect/string` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-threats-in-text.md) for the provider-specific parameters and requirements.

