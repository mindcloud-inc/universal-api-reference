# Create Credential with Emelia

Creates LinkedIn scraper credentials in Emelia.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://graphql.emelia.io`
- **Official documentation:** [Create Credential](https://docs-old.emelia.io/#operation-create_credential-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cookie` | body | `string` | yes | LinkedIn session cookie |
| `jsessionid` | body | `string` | no | Optional JSESSIONID value |
| `li_a` | body | `string` | no | Optional li_at token |
| `ua` | body | `string` | no | Optional user agent string |
