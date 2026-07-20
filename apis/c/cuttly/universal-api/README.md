# <img src="https://images.mindcloud.co/apps/icons/cuttly_1774455724797.png" alt="Cutt.ly logo" width="28" height="28"> Cutt.ly: Universal API

Cutt.ly shortens links, manages aliases and branded domains, and returns analytics for shortened URLs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cuttly/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cutt.ly/
- **Vendor API docs:** https://cutt.ly/cuttly-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Link Statistics](actions/get-link-statistics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/get-link-statistics?connectionId=$CONNECTION_ID&stats=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Add Link Tag](actions/add-link-tag.md) | PUT | Adds a tag to a shortened link in Cutt.ly. |
| [Change Link Alias](actions/change-link-alias.md) | PUT | Updates the alias of a shortened link in Cutt.ly. |
| [Change Source URL](actions/change-source-url.md) | PUT | Updates the destination URL of a shortened link in Cutt.ly. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes a shortened link from Cutt.ly. |
| [Remove AB/C Test](actions/remove-abc-test.md) | PUT | Removes an AB/C test from a shortened link in Cutt.ly. |
| [Remove Expiration](actions/remove-expiration.md) | PUT | Removes expiration from a shortened link in Cutt.ly. |
| [Remove Mobile Redirect](actions/remove-mobile-redirect.md) | PUT | Removes a mobile redirect from a shortened link in Cutt.ly. |
| [Remove Unique Clicks](actions/remove-unique-clicks.md) | PUT | Disables unique-click counting for a shortened link in Cutt.ly. |
| [Set AB Test](actions/set-ab-test.md) | PUT | Sets an AB test for a shortened link in Cutt.ly. |
| [Set ABC Test](actions/set-abc-test.md) | PUT | Sets an ABC test for a shortened link in Cutt.ly. |
| [Set Android Deferred Deep Link](actions/set-android-deferred-deep-link.md) | PUT | Sets an Android deferred deep link for a shortened link in Cutt.ly. |
| [Set Click Expiration](actions/set-click-expiration.md) | PUT | Sets click-based expiration for a shortened link in Cutt.ly. |
| [Set Date Expiration](actions/set-date-expiration.md) | PUT | Sets date-based expiration for a shortened link in Cutt.ly. |
| [Set Link Password](actions/set-link-password.md) | PUT | Sets or removes a password for a shortened link in Cutt.ly. |
| [Set Link Title](actions/set-link-title.md) | PUT | Updates the title of a shortened link in Cutt.ly. |
| [Set Mobile Redirect](actions/set-mobile-redirect.md) | PUT | Sets a mobile redirect for a shortened link in Cutt.ly. |
| [Set Unique Clicks](actions/set-unique-clicks.md) | PUT | Sets the unique-click window for a shortened link in Cutt.ly. |
| [Set Unique Clicks to 15 Minutes](actions/set-unique-clicks-to15-minutes.md) | PUT | Enables 15-minute unique clicks for a shortened link in Cutt.ly. |
| [Shorten Link](actions/shorten-link.md) | POST | Creates a shortened link in Cutt.ly. |
| [Shorten Link With Alias](actions/shorten-link-with-alias.md) | POST | Creates a shortened link with a custom alias in Cutt.ly. |
| [Shorten Link With Custom Domain](actions/shorten-link-with-custom-domain.md) | POST | Creates a shortened link with a custom domain in Cutt.ly. |
| [Shorten Link With Public Stats](actions/shorten-link-with-public-stats.md) | POST | Creates a shortened link with public click stats in Cutt.ly. |

### Link Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Link Statistics](actions/get-link-statistics.md) | GET | Retrieves click statistics for a shortened link in Cutt.ly. |
| [Get Link Statistics By Date Range](actions/get-link-statistics-by-date-range.md) | GET | Retrieves date-range click statistics for a shortened link in Cutt.ly. |

