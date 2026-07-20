# Create Crawl Job with Scrapeless

Creates a new crawl job in Scrapeless.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/crawler/crawl`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Create Crawl Job](https://apidocs.scrapeless.com/api-17509010)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The base URL to start crawling from |
| `limit` | body | `number` | no | Maximum number of pages to crawl. Default limit is 10000. |
| `excludePaths[]` | body | `array<string>` | no | URL pathname regex patterns that exclude matching URLs from the crawl. For example, if you set "excludePaths": ["blog/.*"] for the base URL firecrawl.dev, any results matching that pattern will be excluded, such as https://www.scrapeless.com/blog/firecrawl-launch-week-1-recap. |
| `includePaths[]` | body | `array<string>` | no | URL pathname regex patterns that include matching URLs in the crawl. Only the paths that match the specified patterns will be included in the response. For example, if you set "includePaths": ["blog/.*"] for the base URL firecrawl.dev, only results matching that pattern will be included, such as https://www.scrapeless.com/blog/firecrawl-launch-week-1-recap. |
| `maxDepth` | body | `number` | no | Maximum depth to crawl relative to the base URL. Basically, the max number of slashes the pathname of a scraped URL may contain. |
| `maxDiscoveryDepth` | body | `number` | no | Maximum depth to crawl based on discovery order. The root site and sitemapped pages has a discovery depth of 0. For example, if you set it to 1, and you set ignoreSitemap, you will only crawl the entered URL and all URLs that are linked on that page. |
| `ignoreSitemap` | body | `boolean` | no | Ignore the website sitemap when crawling |
| `ignoreQueryParameters` | body | `boolean` | no | Do not re-scrape the same path with different (or none) query parameters |
| `deduplicateSimilarURLs` | body | `boolean` | no | Controls whether similar URLs should be deduplicated. |
| `regexOnFullURL` | body | `boolean` | no | Controls whether the regular expression should be applied to the full URL. |
| `allowBackwardLinks` | body | `boolean` | no | By default, the crawl skips sublinks that aren’t part of the URL hierarchy you specify. For example, crawling https://example.com/products/ wouldn’t capture pages under https://example.com/promotions/deal-567. To include such links, enable the `allowBackwardLinks` parameter. |
| `allowExternalLinks` | body | `boolean` | no | Allows the crawler to follow links to external websites. |
| `delay` | body | `number` | no | Delay in seconds between scrapes. This helps respect website rate limits. |
| `scrapeOptions` | body | `object` | no | — |
| `scrapeOptions.formats[]` | body | `array<string>` | no | Formats to include in the output. |
| `scrapeOptions.onlyMainContent` | body | `boolean` | no | Only return the main content of the page excluding headers, navs, footers, etc. |
| `scrapeOptions.includeTags[]` | body | `array<string>` | no | Tags to include in the output. |
| `scrapeOptions.excludeTags[]` | body | `array<string>` | no | Tags to exclude from the output. |
| `scrapeOptions.headers` | body | `object` | no | Headers to send with the request. Can be used to send cookies, user-agent, etc. |
| `scrapeOptions.waitFor` | body | `number` | no | Specify a delay in milliseconds before fetching the content, allowing the page sufficient time to load. |
| `scrapeOptions.timeout` | body | `number` | no | Timeout in milliseconds for the request |
| `browserOptions` | body | `object` | no | — |
| `browserOptions.sessionName` | body | `string` | no | Set a name for your session to facilitate searching and viewing in the historical session list. |
| `browserOptions.sessionTTL` | body | `string` | no | Controls the session duration and automatically closes the browser instance after timeout. Measured in seconds (s), defaults to 180 seconds (3 minutes), customizable between 60 seconds (1 minute) and 900 seconds (recommended maximum 15 minutes, but longer times can be set). Once the specified TTL is reached, the session will expire and Scraping Browser will close the browser instance to free resources. |
| `browserOptions.sessionRecording` | body | `string` | no | Whether to enable session recording. When enabled, the entire browser session execution process will be automatically recorded, and after the session is completed, it can be replayed and viewed in the historical session list details. Defaults to false. |
| `browserOptions.proxyCountry` | body | `string` | no | Sets the target country/region for the proxy, sending requests via an IP address from that region. You can specify a country code (e.g., US for the United States, GB for the United Kingdom, ANY for any country). See country codes for all supported options. |
| `browserOptions.proxyURL` | body | `string` | no | Used to set the browser’s proxy URL, for example: http://user:pass@ip:port. If this parameter is set, all other proxy_* parameters will be ignored.  - 💡Custom proxy functionality is currently only available to Enterprise and Enterprise Enhanced subscription users Upgrade Now - 💡Enterprise-level custom users can contact us to use custom proxies. |
| `browserOptions.fingerprint` | body | `string` | no | A browser fingerprint is a nearly unique “digital fingerprint” created using your browser and device configuration information, which can be used to track your online activity even without cookies. Fortunately, configuring fingerprints in Scraping Browser is optional. We offer deep customization of browser fingerprints, such as core parameters like browser user agent, time zone, language, and screen resolution, and support extending functionality through custom launch parameters. Suitable for multi-account management, data collection, and privacy protection scenarios, using scrapeless’s own Chromium browser completely avoids detection. By default, our Scraping Browser service generates a random fingerprint for each session. Reference |
