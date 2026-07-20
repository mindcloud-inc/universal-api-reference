# Extract Emails From URLs with Anyleads

Retrieves emails from a website URL in Anyleads.

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/extract-emails-from-urls`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [Extract Emails From URLs](https://docs.anyleads.com/product/en/email-phone-social-media-extractor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Website URL to scan for emails, phones, and social profiles. |
