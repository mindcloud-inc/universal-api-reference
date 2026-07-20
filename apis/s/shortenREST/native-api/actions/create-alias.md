# Create Alias with Shorten.REST

Creates a new alias in Shorten.REST.

## Endpoint

- **Method:** `POST`
- **Path:** `/aliases`
- **Base URL:** `https://api.shorten.rest`
- **Official documentation:** [Create Alias](https://docs.shorten.rest/#POST--aliases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainName` | query | `string` | no | The domain to attach the alias to, without http/https or trailing slash. |
| `aliasName` | query | `string` | no | Optional alias value without a leading slash. Leave blank to let Shorten.REST generate one. |
| `destinations` | body | `list<object>` | no | List of destination objects. Each object should include at least a url and may also include country or os. |
| `metatags` | body | `list<object>` | no | Optional list of meta tag objects with name and content fields. |
| `snippets` | body | `list<object>` | no | Optional list of snippet objects with id and parameters. |
