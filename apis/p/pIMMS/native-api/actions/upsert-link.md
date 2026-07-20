# Upsert Link with PIMMS

Updates an existing deep link in PIMMS, or creates one.

## Endpoint

- **Method:** `PUT`
- **Path:** `/links/upsert`
- **Base URL:** `https://api.pimms.io`
- **Official documentation:** [Upsert Link](https://pimms.apidocumentation.com/reference#tag/links/PUT/links/upsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Destination URL the deep link redirects to. Supports standard webpages and in-app routing for mobile apps. |
| `domain` | body | `string` | no | Custom domain for your branded deep link. Defaults to the workspace’s primary domain or 'pim.ms'. |
| `key` | body | `string` | no | Custom slug for the short URL. If omitted, an automatic 7-character key is generated. |
| `externalId` | body | `string` | no | External identifier for syncing link data with your internal CRM or analytics tools. Passed in query parameters prefixed by 'ext_'. |
| `prefix` | body | `string` | no | Custom URL path prefix for grouping auto-generated slugs (e.g., '/promo/' resulting in '/promo/abc123'). Ignored if 'key' is specified. |
| `trackConversion` | body | `boolean` | no | Enable detailed conversion tracking to attribute actions like signups or purchases directly to this link. |
| `archived` | body | `boolean` | no | Archive the link to hide it from primary analytics while keeping it active for redirects. |
| `tagIds` | body | `string` | no | List of existing tag IDs to categorize and filter links by campaigns, audiences, or purposes. |
| `tagNames` | body | `string` | no | New or existing tag names to assign for improved readability and organization. |
| `comments` | body | `string` | no | Internal notes for team members about link context, purpose, or specific campaign details. |
| `expiresAt` | body | `string` | no | ISO 8601 timestamp when the link should stop redirecting users. |
| `expiredUrl` | body | `string` | no | Fallback destination URL after link expiration, preventing broken user experiences. |
| `title` | body | `string` | no | Custom Open Graph (OG) title to optimize social media sharing and improve link previews. |
| `description` | body | `string` | no | Custom Open Graph description for better engagement when shared on social platforms. |
| `image` | body | `string` | no | URL for a custom OG image to enhance visual appeal and click-through rates on social media. |
| `video` | body | `string` | no | Custom video URL for rich media previews via Open Graph when sharing links. |
| `ios` | body | `string` | no | The iOS destination URL for the short link for iOS device targeting. |
| `android` | body | `string` | no | The Android destination URL for the short link for Android device targeting. |
| `doIndex` | body | `boolean` | no | Allow search engine indexing of the deep link. Defaults to false for privacy. |
| `utm_source` | body | `string` | no | UTM source parameter for tracking the origin of traffic (e.g., 'linkedin', 'facebook', 'newsletter'). |
| `utm_medium` | body | `string` | no | UTM medium parameter identifying traffic medium such as 'post', 'email', 'social', or 'cpc'. |
| `utm_campaign` | body | `string` | no | UTM campaign parameter for tracking specific marketing initiatives or promotions. |
| `utm_term` | body | `string` | no | UTM term parameter for keyword analysis, often used in paid search campaigns. |
| `utm_content` | body | `string` | no | UTM content parameter distinguishing different content variations or link placements within a campaign. |
| `ref` | body | `string` | no | Custom referral parameter appended as '?ref=' for downstream attribution and analysis. |
| `webhookIds[]` | body | `array<string>` | no | Webhook IDs to trigger real-time notifications upon link clicks, ideal for integrating with analytics or marketing automation tools. Send multiple values as a array. |
