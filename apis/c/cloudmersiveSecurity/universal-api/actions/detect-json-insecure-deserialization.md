# Cloudmersive Security: Detect JSON Insecure Deserialization

Detects JSON insecure deserialization attacks in Cloudmersive Security.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-json-insecure-deserialization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Security `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-json-insecure-deserialization?connectionId=$CONNECTION_ID&jsonText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jsonText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-json-insecure-deserialization?${params}`, {
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
| `jsonText` | string | yes | JSON text input to scan for insecure deserialization attacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ContainedJsonInsecureDeserializationAttack": true,
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
| `ContainedJsonInsecureDeserializationAttack` | boolean |  |
| `OriginalInput` | string |  |
| `Successful` | boolean |  |

## Native endpoint

Through the native Cloudmersive Security API, this operation is `POST /security/threat-detection/content/insecure-deserialization/json/detect/string` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-json-insecure-deserialization.md) for the provider-specific parameters and requirements.

