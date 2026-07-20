# Update Alias with Shorten.REST

Updates an existing alias in Shorten.REST.

## Endpoint

- **Method:** `PUT`
- **Path:** `/aliases`
- **Base URL:** `https://api.shorten.rest`
- **Official documentation:** [Update Alias](https://docs.shorten.rest/#PUT--aliases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainName` | query | `string` | no | The domain which the alias belongs to, without http/https or trailing slash. |
| `aliasName` | query | `string` | yes | The alias value without a leading slash. |
| `destinations` | body | `list<object>` | no | Optional list of destination objects. When provided, the full destinations block is replaced. |
| `metatags` | body | `list<object>` | no | Optional list of meta tag objects with name and content fields. When provided, the full meta tags block is replaced. |
| `snippets` | body | `list<object>` | no | Optional list of snippet objects with id and parameters. When provided, the full snippets block is replaced. |
