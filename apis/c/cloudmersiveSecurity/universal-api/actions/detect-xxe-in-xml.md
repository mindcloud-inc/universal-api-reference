# Cloudmersive Security: Detect XXE in XML

Detects XXE threats in XML with Cloudmersive Security.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-xxe-in-xml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Security `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-xxe-in-xml?connectionId=$CONNECTION_ID&xmlText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "xmlText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-xxe-in-xml?${params}`, {
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
| `xmlText` | string | yes | XML text input to scan for XML External Entity attacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ContainedXxe": true,
      "Successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ContainedXxe` | boolean |  |
| `Successful` | boolean |  |

## Native endpoint

Through the native Cloudmersive Security API, this operation is `POST /security/threat-detection/content/xxe/detect/xml/string` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-xxe-in-xml.md) for the provider-specific parameters and requirements.

