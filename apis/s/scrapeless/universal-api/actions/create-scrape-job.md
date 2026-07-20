# Scrapeless: Create Scrape Job

Creates a new scrape job in Scrapeless.

```
POST https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-scrape-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-scrape-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-scrape-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The URL to scrape |
| `formats[]` | array<string> | no | Formats to include in the output. |
| `onlyMainContent` | boolean | no | Only return the main content of the page excluding headers, navs, footers, etc. |
| `includeTags[]` | array<string> | no | Tags to include in the output. |
| `excludeTags[]` | array<string> | no | Tags to exclude from the output. |
| `headers` | object | no | Headers to send with the request. Can be used to send cookies, user-agent, etc. |
| `waitFor` | number | no | Specify a delay in milliseconds before fetching the content, allowing the page sufficient time to load. |
| `timeout` | number | no | Timeout in milliseconds for the request |
| `browserOptions` | object | no |  |
| `browserOptions.sessionName` | string | no | Set a name for your session to facilitate searching and viewing in the historical session list. |
| `browserOptions.sessionTTL` | string | no | Controls the session duration and automatically closes the browser instance after timeout. Measured in seconds (s), defaults to 180 seconds (3 minutes), customizable between 60 seconds (1 minute) and 900 seconds (recommended maximum 15 minutes, but longer times can be set). Once the specified TTL is reached, the session will expire and Scraping Browser will close the browser instance to free resources. |
| `browserOptions.sessionRecording` | string | no | Whether to enable session recording. When enabled, the entire browser session execution process will be automatically recorded, and after the session is completed, it can be replayed and viewed in the historical session list details. Defaults to false. |
| `browserOptions.proxyCountry` | string | no | Sets the target country/region for the proxy, sending requests via an IP address from that region. You can specify a country code (e.g., US for the United States, GB for the United Kingdom, ANY for any country). See country codes for all supported options. |
| `browserOptions.proxyURL` | string | no | Used to set the browser’s proxy URL, for example: http://user:pass@ip:port. If this parameter is set, all other proxy_* parameters will be ignored. - 💡Custom proxy functionality is currently only available to Enterprise and Enterprise Enhanced subscription users Upgrade Now - 💡Enterprise-level custom users can contact us to use custom proxies. |
| `browserOptions.fingerprint` | string | no | A browser fingerprint is a nearly unique “digital fingerprint” created using your browser and device configuration information, which can be used to track your online activity even without cookies. Fortunately, configuring fingerprints in Scraping Browser is optional. We offer deep customization of browser fingerprints, such as core parameters like browser user agent, time zone, language, and screen resolution, and support extending functionality through custom launch parameters. Suitable for multi-account management, data collection, and privacy protection scenarios, using scrapeless’s own Chromium browser completely avoids detection. By default, our Scraping Browser service generates a random fingerprint for each session. Reference |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Scrapeless API, this operation is `POST /api/v2/crawler/scrape` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scrape-job.md) for the provider-specific parameters and requirements.

