# Search Similar Companies with Leadberry

## Endpoint

- **Method:** `POST`
- **Path:** `/data/searchSimilar`
- **Base URL:** `https://app.leadberry.com`
- **Official documentation:** [Search Similar Companies](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | yes | Leadberry company category to search similar companies for. |
| `country` | body | `string` | yes | Country code or country name for the similar-company search. |
| `token` | body | `string` | yes | Leadberry token value read from the app session context. |
