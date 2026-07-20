# Update Site Settings with DatoCMS

## Endpoint

- **Method:** `PUT`
- **Path:** `/site`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Update Site Settings](https://www.datocms.com/docs/content-management-api/resources/site/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes` | body | `object` | yes | Site settings attributes object. |
| `data.attributes.global_seo.site_name` | body | `string` | no | — |
| `data.attributes.global_seo.fallback_seo` | body | `object` | no | — |
| `data.attributes.global_seo.fallback_seo.title` | body | `string` | no | — |
| `data.attributes.global_seo.fallback_seo.description` | body | `string` | no | — |
| `data.attributes.global_seo.fallback_seo.image` | body | `string` | no | — |
| `data.attributes.global_seo.fallback_seo.twitter_card` | body | `string` | no | — |
| `data.attributes.global_seo.title_suffix` | body | `string` | no | — |
| `data.attributes.global_seo.facebook_page_url` | body | `string` | no | — |
| `data.attributes.global_seo.twitter_account` | body | `string` | no | — |
| `data.attributes.locales[]` | body | `array<string>` | no | — |
| `data.attributes.favicon` | body | `string` | no | — |
| `data.attributes.global_seo` | body | `object` | no | — |
| `data.attributes.name` | body | `string` | no | — |
| `data.attributes.no_index` | body | `boolean` | no | — |
| `data.attributes.theme` | body | `object` | no | — |
| `data.attributes.force_use_of_sandbox_environments` | body | `boolean` | no | — |
| `data.attributes.ip_tracking_enabled` | body | `boolean` | no | — |
| `data.attributes.require_2fa` | body | `boolean` | no | — |
| `data.attributes.timezone` | body | `string` | no | — |
