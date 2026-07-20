# <img src="https://images.mindcloud.co/apps/icons/botster_1780330721082.png" alt="Botster logo" width="28" height="28"> Botster: Universal API

Run Botster bots and manage scraping jobs and results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/botster/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://botster.io
- **Vendor API docs:** https://botster.io/info/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botster/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Bots](actions/list-bots.md) | GET | Retrieves the available bots from Botster. |
| [Search Bots](actions/search-bots.md) | GET | Finds bots in Botster by search query. |

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves your remaining Botster credits balance. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Archive Job](actions/archive-job.md) | PUT | Archives an existing job in Botster. |
| [Delete Job](actions/delete-job.md) | DELETE | Deletes an existing job from Botster. |
| [Get Job](actions/get-job.md) | GET | Retrieves a Botster job and its runs. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves the jobs in your Botster account. |
| [Restart Job](actions/restart-job.md) | PUT | Restarts an existing job in Botster. |
| [Run Bulk DNS Lookup](actions/run-bulk-dns-lookup.md) | POST | Creates a Botster bulk DNS lookup job. |
| [Run Bulk Whois Lookup](actions/run-bulk-whois-lookup.md) | POST | Creates a Botster bulk WHOIS lookup job. |
| [Run Company Website Finder](actions/run-company-website-finder.md) | POST | Creates a Botster company website lookup job. |
| [Run Contact Data Scraper](actions/run-contact-data-scraper.md) | POST | Creates a Botster contact data extraction job. |
| [Run Find Subdomains](actions/run-find-subdomains.md) | POST | Creates a Botster subdomain discovery job. |
| [Run Google Maps Places Scraper](actions/run-google-maps-places-scraper.md) | POST | Creates a Botster Google Maps place extraction job. |
| [Run Google Maps Reviews Scraper](actions/run-google-maps-reviews-scraper.md) | POST | Creates a Botster Google review extraction job. |
| [Run Google Pagespeed Bulk Checker](actions/run-google-pagespeed-bulk-checker.md) | POST | Creates a Botster Google PageSpeed checking job. |
| [Run Google Rank Checker](actions/run-google-rank-checker.md) | POST | Creates a Botster Google rank checking job. |
| [Run Google Search Scraper](actions/run-google-search-scraper.md) | POST | Creates a Botster Google search results extraction job. |
| [Run Google Search Suggestions Scraper](actions/run-google-search-suggestions-scraper.md) | POST | Creates a Botster Google search suggestions job. |
| [Run LinkedIn Company Finder](actions/run-linked-in-company-finder.md) | POST | Creates a Botster LinkedIn company lookup job. |
| [Run LinkedIn Profile to URL Finder](actions/run-linked-in-profile-to-url-finder.md) | POST | Creates a Botster LinkedIn profile website lookup job. |
| [Run Search Volume and CPC Finder](actions/run-search-volume-and-cpc-finder.md) | POST | Creates a Botster keyword search volume and CPC job. |
| [Run TikTok Profile Extractor](actions/run-tik-tok-profile-extractor.md) | POST | Creates a Botster TikTok profile extraction job. |
| [Run Website Traffic Checker](actions/run-website-traffic-checker.md) | POST | Creates a Botster website traffic estimate job. |
| [Run YouTube Search Scraper](actions/run-you-tube-search-scraper.md) | POST | Creates a Botster YouTube search extraction job. |
| [Unarchive Job](actions/unarchive-job.md) | PUT | Unarchives an existing job in Botster. |

### Run

| Action | Method | Description |
| --- | --- | --- |
| [Delete Run](actions/delete-run.md) | DELETE | Deletes an existing run from Botster. |
| [Get Run](actions/get-run.md) | GET | Retrieves result data for a Botster run. |

