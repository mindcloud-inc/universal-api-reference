# Generate SSR Install Instructions with Appzi

Generates SSR install snippets for Appzi.

## Endpoint

- **Method:** `GET`
- **Path:** `https://docs.appzi.io/installation/`
- **Base URL:** `https://api.appzi.io`
- **Official documentation:** [Generate SSR Install Instructions](https://docs.appzi.io/installation/#server-side-rendering-ssr)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portalToken` | query | `string` | yes | Portal token inserted into the generated SSR install snippet. |
| `framework` | query | `string` | yes | SSR framework documented by Appzi: next-app-router, next-pages-router, nuxt, sveltekit, or jekyll. |
