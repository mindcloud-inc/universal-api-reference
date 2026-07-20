# Fetch Storage Bulk Items with Crawlbase

Retrieves stored pages in bulk from Crawlbase.

## Endpoint

- **Method:** `POST`
- **Path:** `/storage/bulk`
- **Base URL:** `https://api.crawlbase.com`
- **Official documentation:** [Fetch Storage Bulk Items](https://crawlbase.com/docs/cloud-storage/bulk/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rids` | body | `string<string>` | yes | Array of storage RIDs to retrieve. Crawlbase processes a maximum of 100 RIDs per request. Send multiple values as a array. |
| `auto_delete` | body | `boolean` | no | Whether Crawlbase should delete fetched storage items after retrieval. Defaults to false. |
