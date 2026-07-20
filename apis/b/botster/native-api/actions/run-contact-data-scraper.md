# Run Contact Data Scraper with Botster

Creates a Botster contact data extraction job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/contact-data-scraper`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Contact Data Scraper](https://botster.io/bots/contact-data-scraper)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `elements[]` | body | `array<string>` | yes | Contact data elements to extract. |
| `input` | body | `string` | yes | Website list. |
| `limit` | body | `string` | yes | How many pages the bot should visit. |
