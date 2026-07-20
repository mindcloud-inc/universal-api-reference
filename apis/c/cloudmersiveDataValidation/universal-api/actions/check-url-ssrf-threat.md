# Cloudmersive Data Validation: Check URL SSRF Threat

Checks a URL for SSRF threats with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/check-url-ssrf-threat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/check-url-ssrf-threat?connectionId=$CONNECTION_ID&request=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/check-url-ssrf-threat?${params}`, {
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
| `request` | object | yes | URL SSRF threat-check request object containing the URL to check. |

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
| `ThreatLevel` | string |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/domain/url/ssrf-threat-check` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-url-ssrf-threat.md) for the provider-specific parameters and requirements.

