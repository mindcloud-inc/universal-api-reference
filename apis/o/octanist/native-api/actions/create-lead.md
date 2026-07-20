# Create Lead with Octanist

Creates a new lead in Octanist.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads`
- **Base URL:** `https://octanist.com/api`
- **Official documentation:** [Create Lead](https://octanist.com/docs/api-reference/endpoint/create-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Lead name. |
| `email` | body | `string` | no | Lead email. |
| `phone` | body | `string` | no | Lead phone number. |
| `custom` | body | `string` | no | Custom lead data. Accepts a string or JSON value. |
| `note` | body | `string` | no | Note to attach to the lead. |
| `website` | body | `string` | no | Lead website URL. |
| `path` | body | `string` | no | Page path associated with the lead. |
| `gclid` | body | `string` | no | Google Ads click ID. |
| `fbc` | body | `string` | no | Meta click ID. |
| `fbp` | body | `string` | no | Meta browser ID. |
| `ga4cid` | body | `string` | no | Google Analytics 4 client ID. |
| `ga4sid` | body | `string` | no | Google Analytics 4 session ID. |
| `utm_source` | body | `string` | no | UTM source value. |
| `utm_medium` | body | `string` | no | UTM medium value. |
| `utm_campaign` | body | `string` | no | UTM campaign value. |
| `ad_storage` | body | `boolean` | no | Ad storage consent flag. |
| `ad_user_data` | body | `boolean` | no | Ad user data consent flag. |
| `ad_personalization` | body | `boolean` | no | Ad personalization consent flag. |
| `analytics_storage` | body | `boolean` | no | Analytics storage consent flag. |
