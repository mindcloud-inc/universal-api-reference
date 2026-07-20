# Bulk Delete Links with Switchy.io

Deletes existing links from Switchy.io by domain and IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/graphql`
- **Base URL:** `https://graphql.switchy.io`
- **Official documentation:** [Bulk Delete Links](https://developers.switchy.io/docs/overview/root-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | — |
| `idsCsv` | body | `string` | yes | Comma-separated link ids within the selected domain |
