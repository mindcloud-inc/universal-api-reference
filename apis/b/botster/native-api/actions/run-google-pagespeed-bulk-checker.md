# Run Google Pagespeed Bulk Checker with Botster

Creates a Botster Google PageSpeed checking job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/google-pagespeed-bulk-checker`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Google Pagespeed Bulk Checker](https://botster.io/bots/google-pagespeed-bulk-checker)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | URLs to check with Google Pagespeed. |
