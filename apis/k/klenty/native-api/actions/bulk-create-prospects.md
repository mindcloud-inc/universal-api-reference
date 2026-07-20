# Bulk Create Prospects with Klenty

Creates prospects in bulk in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Bulk Create Prospects](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_0356ba7595)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Prospects` | body | `list<object>` | yes | List of prospects to create. Each item supports the documented Create Prospect fields. |
