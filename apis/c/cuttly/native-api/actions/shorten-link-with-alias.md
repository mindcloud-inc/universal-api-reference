# Shorten Link With Alias with Cutt.ly

Creates a shortened link with a custom alias in Cutt.ly.

## Endpoint

- **Method:** `GET`
- **Path:** `/api.php`
- **Base URL:** `https://cutt.ly/api`
- **Official documentation:** [Shorten Link With Alias](https://cutt.ly/api-documentation/cuttly-links-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `short` | query | `string` | yes | The full destination URL to shorten. |
| `name` | query | `string` | yes | Requested short-link alias. |
