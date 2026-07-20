# Create Browser Session Task with Scrapeless

Creates a browser session task in Scrapeless.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/browser`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Create Browser Session Task](https://apidocs.scrapeless.com/api-24826702)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionTTL` | query | `string` | yes | The session_ttl parameter controls the duration of the session and automatically closes the browser instance after the session times out. The unit of session_ttl is seconds (S), with a default value of 180 seconds (i.e., 3 minutes), and can be customized between 60 seconds (1 minute) and 900 seconds (15 minutes). When the specified TTL time is reached, the session will become invalid, and Scraping Browser will close the browser instance to release resources. Please set the session_ttl reasonably according to the task requirements to ensure that the operations are completed before the session times out. |
| `sessionName` | query | `string` | no | Set a name for your session to facilitate searching and viewing in the historical session list. |
| `sessionRecording` | query | `boolean` | no | Whether to enable session recording. When enabled, the entire browser session execution process will be automatically recorded, and after the session is completed, it can be replayed and viewed in the historical session list details. |
| `proxyURL` | query | `string` | no | Used to set the browser’s proxy URL, for example: http://user:pass@ip:port. If this parameter is set, all other proxy* parameters will be ignored. Required if `proxyCountry` not set. > 💡Custom proxy functionality is currently only available to subscribers. [Upgrade here](https://www.scrapeless.com/en/pricing) |
| `proxyCountry[]` | query | `array<string>` | no | The proxyCountry parameter is used to set the target country of the proxy, making the request sent through the IP address of that region. You can customize the proxy source by specifying a country code for proxyCountry (e.g., US for the United States, GB for the United Kingdom, ANY for any country). Scraping Browser will provide the corresponding IP address based on the specified country, which helps meet regional access restrictions or geographic positioning needs. Required if `proxyURL` not set. |
| `proxyState` | query | `string` | no | Specifies the target state/province within the selected country for more granular proxy routing. Must be used in conjunction with `proxyCountry`. Accepts state codes (e.g., `CA` for California, `NY` for New York). Available for select countries with defined state/province divisions. [learn mor](https://docs.scrapeless.com/en/proxies/features/proxy) |
| `proxyCity` | query | `string` | no | Specifies the target city within the selected state/province for city-level proxy routing. Must be used in conjunction with `proxyCountry` and `proxyState`. Provides the most precise geographic targeting. Availability depends on proxy infrastructure in specific cities. |
| `extensionIds` | query | `string` | no | setup browser extension by extension id, separate by comma for multiple extensions |
| `fingerprint` | query | `string` | no | Custom browser fingerprint with URL encoded JSON string format, see below for full schema. note that the`ws/get`type of request cannot have a request body, the`Body Params`below only for display purpose |
