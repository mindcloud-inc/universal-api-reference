# Enrich Company with FindyMail

Retrieves company enrichment data from FindyMail.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/search/company`
- **Base URL:** `https://app.findymail.com`
- **Official documentation:** [Enrich Company](https://www.findymail.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Company domain to enrich, for example stripe.com. |
