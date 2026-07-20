# List OAI Records with Rijksmuseum

## Endpoint

- **Method:** `GET`
- **Path:** `/oai`
- **Base URL:** `https://data.rijksmuseum.nl`
- **Official documentation:** [List OAI Records](https://data.rijksmuseum.nl/docs/oai-pmh/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadataPrefix` | query | `string` | no | OAI-PMH metadata format prefix. Defaults to oai_dc. |
| `set` | query | `string` | no | Optional OAI-PMH set spec identifier to harvest a curated object set. |
| `from` | query | `string` | no | Optional UTC lower bound timestamp, such as 2026-01-01T00:00:00Z. |
| `until` | query | `string` | no | Optional UTC upper bound timestamp, such as 2026-04-01T00:00:00Z. |
| `resumptionToken` | query | `string` | no | Token from a previous OAI-PMH ListRecords response for pagination. |
