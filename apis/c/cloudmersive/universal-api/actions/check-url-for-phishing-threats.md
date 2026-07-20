# Cloudmersive: Check URL for Phishing Threats

Checks a URL for phishing threats in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/check-url-for-phishing-threats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/check-url-for-phishing-threats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/check-url-for-phishing-threats?${params}`, {
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
| `URL` | string | no | URL to scan for phishing threats. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cleanUrl": true,
      "threatType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cleanUrl` | boolean |  |
| `threatType` | string |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/domain/url/phishing-threat-check` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-url-for-phishing-threats.md) for the provider-specific parameters and requirements.

