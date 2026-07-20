# Cloudmersive Security: Detect SSRF URL Threat

Checks a URL for SSRF threats in Cloudmersive Security.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-ssrf-url-threat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Security `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-ssrf-url-threat?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/detect-ssrf-url-threat?${params}`, {
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
| `url` | string | yes | URL to check for SSRF threat risk. |
| `blockedDomains[]` | array<string> | no | Optional domains to block. Each entry blocks that domain and its subdomains. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CleanURL": true,
      "ThreatLevel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CleanURL` | boolean |  |
| `ThreatLevel` | string | Possible values include High, Medium, Low, and None. |

## Native endpoint

Through the native Cloudmersive Security API, this operation is `POST /security/threat-detection/network/url/ssrf/detect` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-ssrf-url-threat.md) for the provider-specific parameters and requirements.

