# Create Domain with Short.io

Creates a new domain in Short.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/domains`
- **Base URL:** `https://api.short.io`
- **Official documentation:** [Create Domain](https://developers.short.io/reference/post_domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | body | `string` | yes | — |
| `hideReferer` | body | `boolean` | no | — |
| `linkType` | body | `list<string>` | no | Accepted values: `eight-char`, `four-char`, `increment`, `random`, `secure`, `ten-char`. |
