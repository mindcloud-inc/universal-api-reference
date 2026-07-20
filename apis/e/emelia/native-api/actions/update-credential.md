# Update Credential with Emelia

Updates LinkedIn scraper credentials in Emelia.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://graphql.emelia.io`
- **Official documentation:** [Update Credential](https://docs-old.emelia.io/#operation-update_credential-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cookie` | body | `string` | yes | LinkedIn session cookie |
| `id` | body | `string` | yes | Credential identifier |
| `jsessionid` | body | `string` | no | Optional JSESSIONID value |
| `li_a` | body | `string` | no | Optional li_at token |
| `ua` | body | `string` | no | Optional user agent string |
