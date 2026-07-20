# Scrapeless: Create Browser Session Task

Creates a browser session task in Scrapeless.

```
POST https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-browser-session-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-browser-session-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionTTL": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-browser-session-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionTTL": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionTTL` | string | yes | The session_ttl parameter controls the duration of the session and automatically closes the browser instance after the session times out. The unit of session_ttl is seconds (S), with a default value of 180 seconds (i.e., 3 minutes), and can be customized between 60 seconds (1 minute) and 900 seconds (15 minutes). When the specified TTL time is reached, the session will become invalid, and Scraping Browser will close the browser instance to release resources. Please set the session_ttl reasonably according to the task requirements to ensure that the operations are completed before the session times out. |
| `sessionName` | string | no | Set a name for your session to facilitate searching and viewing in the historical session list. |
| `sessionRecording` | boolean | no | Whether to enable session recording. When enabled, the entire browser session execution process will be automatically recorded, and after the session is completed, it can be replayed and viewed in the historical session list details. |
| `proxyURL` | string | no | Used to set the browser’s proxy URL, for example: http://user:pass@ip:port. If this parameter is set, all other proxy* parameters will be ignored. Required if `proxyCountry` not set. > 💡Custom proxy functionality is currently only available to subscribers. [Upgrade here](https://www.scrapeless.com/en/pricing) |
| `proxyCountry[]` | array<string> | no | The proxyCountry parameter is used to set the target country of the proxy, making the request sent through the IP address of that region. You can customize the proxy source by specifying a country code for proxyCountry (e.g., US for the United States, GB for the United Kingdom, ANY for any country). Scraping Browser will provide the corresponding IP address based on the specified country, which helps meet regional access restrictions or geographic positioning needs. Required if `proxyURL` not set. |
| `proxyState` | string | no | Specifies the target state/province within the selected country for more granular proxy routing. Must be used in conjunction with `proxyCountry`. Accepts state codes (e.g., `CA` for California, `NY` for New York). Available for select countries with defined state/province divisions. [learn mor](https://docs.scrapeless.com/en/proxies/features/proxy) |
| `proxyCity` | string | no | Specifies the target city within the selected state/province for city-level proxy routing. Must be used in conjunction with `proxyCountry` and `proxyState`. Provides the most precise geographic targeting. Availability depends on proxy infrastructure in specific cities. |
| `extensionIds` | string | no | setup browser extension by extension id, separate by comma for multiple extensions |
| `fingerprint` | string | no | Custom browser fingerprint with URL encoded JSON string format, see below for full schema. note that the`ws/get`type of request cannot have a request body, the`Body Params`below only for display purpose |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | if task created |
| `taskId` | string | session taskId |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /api/v2/browser` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-browser-session-task.md) for the provider-specific parameters and requirements.

