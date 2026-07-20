# Cloudmersive Virus Scan: Scan Website for Threats

Scans a website for malicious content with Cloudmersive Virus Scan.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/scan-website-for-threats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Virus Scan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/scan-website-for-threats?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/scan-website-for-threats?${params}`, {
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
| `url` | string | yes | Website URL to scan for malicious content and threats. Must begin with http:// or https://. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CleanResult": true,
      "FoundViruses": [
        {
          "FileName": "Ava Chen",
          "VirusName": "Ava Chen"
        }
      ],
      "WebsiteHttpResponseCode": 1,
      "WebsiteThreatType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CleanResult` | boolean | True when the website scan finds no malicious content or threats. |
| `FoundViruses` | array<object> | Viruses found in website content, when any are detected. |
| `FoundViruses[].FileName` | string | File name or content item where the virus was found. |
| `FoundViruses[].VirusName` | string | Detected virus or malware name. |
| `WebsiteHttpResponseCode` | number | HTTP response code observed while scanning the website. |
| `WebsiteThreatType` | string | Threat category detected for the website, when any. |

## Native endpoint

Through the native Cloudmersive Virus Scan API, this operation is `POST /virus/scan/website` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scan-website-for-threats.md) for the provider-specific parameters and requirements.

