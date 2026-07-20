# Search Subscribers with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriber.search/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [Search Subscribers](https://chmyos.notion.site/Search-Subscribers-5e9d41998a5945d4912d9bb1cd228a51)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EmailAddress` | body | `string` | yes | Exact or partial email address to search for |
