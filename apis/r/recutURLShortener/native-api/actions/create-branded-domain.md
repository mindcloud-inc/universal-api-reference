# Create Branded Domain with Recut URL Shortener

Creates a branded domain in Recut URL Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain/add`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Create Branded Domain](https://app.recut.in/developers#create-a-branded-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Branded domain to add |
| `redirectroot` | body | `string` | no | Redirect URL for the domain root |
| `redirect404` | body | `string` | no | Redirect URL for 404 pages |
