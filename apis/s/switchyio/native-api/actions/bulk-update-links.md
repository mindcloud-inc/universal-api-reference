# Bulk Update Links with Switchy.io

Updates existing links in Switchy.io by domain and IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/graphql`
- **Base URL:** `https://graphql.switchy.io`
- **Official documentation:** [Bulk Update Links](https://developers.switchy.io/docs/overview/root-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | — |
| `idsCsv` | body | `string` | yes | Comma-separated link ids within the selected domain |
| `url` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `description` | body | `string` | no | — |
