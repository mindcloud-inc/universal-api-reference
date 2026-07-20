# Update Domain Settings with Once.to

Updates an existing domain in Once.to.

## Endpoint

- **Method:** `PUT`
- **Path:** `/domains/:id`
- **Base URL:** `https://once.to/api/public/v1`
- **Official documentation:** [Update Domain Settings](https://docs.once.to/en/api/v1/endpoints/domains-put/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the domain to update. |
| `name` | body | `string` | yes | Existing domain name. Once.to requires it to remain unchanged. |
| `description` | body | `string` | no | Optional remarks for the domain. |
| `rootRedirUrl` | body | `string` | no | Optional redirect URL for the domain root. |
| `notFoundRedirUrl` | body | `string` | no | Optional redirect URL when a slug is not found. |
| `default` | body | `boolean` | no | Whether to make this domain the default. |
