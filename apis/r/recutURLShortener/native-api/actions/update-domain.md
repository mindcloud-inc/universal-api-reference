# Update Domain with Recut URL Shortener

Updates an existing branded domain in Recut URL Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/domain/:id/update`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Update Domain](https://app.recut.in/developers#update-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Domain ID |
| `redirectroot` | body | `string` | no | Redirect URL for the domain root |
| `redirect404` | body | `string` | no | Redirect URL for 404 pages |
