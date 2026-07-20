# <img src="https://images.mindcloud.co/apps/icons/2smart-icon-square_1776362896782.png" alt="2Smart Cloud logo" width="28" height="28"> 2Smart Cloud: Universal API

2Smart Cloud is a cloud platform for connecting and supporting Internet of Things devices, including vendor-side product, firmware, layout, dashboard, statistics, and notification management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smartCloud/latest
- **Actions:** 235
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://2smart.com/
- **Vendor API docs:** https://cloud.2smart.com/swagger/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get vendor info](actions/get-vendor-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-vendor-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (235)

### Aggregated Value

| Action | Method | Description |
| --- | --- | --- |
| [Aggregated value for topic](actions/get-admin-aggregated-value.md) | GET |  |
| [Aggregated value for topic](actions/get-share-v1-aggregated-value.md) | GET |  |
| [List timelines](actions/get-timelines-aggregated-value.md) | GET |  |

### Api Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create api token](actions/create-vendor-api-tokens.md) | POST |  |
| [Delete api token](actions/delete-vendor-api-tokens-by-id-delete.md) | DELETE |  |
| [Show api token](actions/get-vendor-api-tokens-by-id.md) | GET |  |
| [List api tokens](actions/list-vendor-api-tokens.md) | GET |  |
| [Update api token](actions/update-vendor-api-tokens-by-id-update.md) | PUT |  |

### Apple

| Action | Method | Description |
| --- | --- | --- |
| [Login mobile user with Apple](actions/create-sessions-apple.md) | POST |  |
| [Login vendor with Apple](actions/create-vendor-login-apple.md) | POST |  |

### Binaries

| Action | Method | Description |
| --- | --- | --- |
| [Binary upload](actions/create-vendor-binaries.md) | POST |  |

### Binaries Mock

| Action | Method | Description |
| --- | --- | --- |
| [Binary mock upload](actions/create-vendor-binaries-mock.md) | POST |  |

### Biometric

| Action | Method | Description |
| --- | --- | --- |
| [Login mobile user with biometric key](actions/create-sessions-biometric.md) | POST |  |
| [Delete biometric key for device](actions/create-users-delete-biometric.md) | POST |  |
| [Update mobile user with biometric](actions/create-users-update-biometric.md) | POST |  |
| [Check if user has biometric key](actions/list-users-check-biometric.md) | GET |  |

### Build Parts

| Action | Method | Description |
| --- | --- | --- |
| [Create build part](actions/create-vendor-build-parts.md) | POST |  |
| [Delete build part](actions/delete-vendor-build-parts-by-id-delete.md) | DELETE |  |
| [Update build part](actions/factory-vendor-build-parts-by-id-factory.md) | PUT |  |
| [Update build part](actions/update-vendor-build-parts-by-id.md) | PUT |  |

### Builds

| Action | Method | Description |
| --- | --- | --- |
| [Build upload](actions/create-vendor-builds.md) | POST |  |

### Bulk

| Action | Method | Description |
| --- | --- | --- |
| [Create phone number](actions/create-phone-numbers-bulk.md) | POST |  |

### Bulk Add

| Action | Method | Description |
| --- | --- | --- |
| [Bulk add favorite widgets to groups](actions/create-favorite-widget-groups-bulk-add.md) | POST |  |

### Bulk Delete

| Action | Method | Description |
| --- | --- | --- |
| [Bulk delete favorite widgets](actions/create-favorite-widgets-bulk-delete.md) | POST |  |
| [Bulk Delete shared device](actions/create-share-link-devices-bulk-delete.md) | POST |  |
| [Bulk Delete shared device](actions/create-shared-devices-bulk-delete.md) | POST |  |

### Change Password

| Action | Method | Description |
| --- | --- | --- |
| [Change password mobile user](actions/create-users-change-password.md) | POST |  |
| [Update vendor](actions/create-vendor-change-password.md) | POST |  |

### Check Biometric

| Action | Method | Description |
| --- | --- | --- |
| [Check if there is biometric keys for this device](actions/create-devices-by-device-id-check-biometric.md) | POST |  |

### Check Exists

| Action | Method | Description |
| --- | --- | --- |
| [Register mobile user](actions/get-users-check-exists.md) | GET |  |

### Check Reset Password Token

| Action | Method | Description |
| --- | --- | --- |
| [Check reset vendor password token](actions/create-vendor-check-reset-password-token.md) | POST |  |

### Clear Abbreviations

| Action | Method | Description |
| --- | --- | --- |
| [Clear products abbreviations](actions/get-admin-products-clear-abbreviations.md) | GET |  |

### Clear Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Clear phone number of mobile user](actions/create-users-clear-phone-number.md) | POST |  |

### Contact Us

| Action | Method | Description |
| --- | --- | --- |
| [Send `contact us` email](actions/create-landing-emails-contact-us.md) | POST |  |

### Credentials

| Action | Method | Description |
| --- | --- | --- |
| [Create favorite widget group](actions/create-devices-by-device-id-credentials.md) | POST |  |

### Csrf Token

| Action | Method | Description |
| --- | --- | --- |
| [Get CSRF Token](actions/list-csrf-token.md) | GET |  |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [Archive/Unarchive layout](actions/archive-vendor-dashboards-by-id-archive.md) | DELETE |  |
| [Create dashboard](actions/create-vendor-dashboards.md) | POST |  |
| [Delete dashboard](actions/delete-vendor-dashboards-by-id-delete.md) | DELETE |  |
| [Show dashboard](actions/get-vendor-dashboards-by-id.md) | GET |  |
| [List dashboards](actions/list-vendor-dashboards.md) | GET |  |
| [Update dashboard](actions/update-vendor-dashboards-by-id-update.md) | PUT |  |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [List devices](actions/list-admin-devices.md) | GET |  |

### Facebook

| Action | Method | Description |
| --- | --- | --- |
| [Login mobile user with Facebook](actions/create-sessions-facebook.md) | POST |  |
| [Login vendor with Facebook](actions/create-vendor-login-facebook.md) | POST |  |

### Favorite Widget Groups

| Action | Method | Description |
| --- | --- | --- |
| [Bulk update favorite widgets groups positions](actions/bulk-update-favorite-widget-groups-bulk-update.md) | PUT |  |
| [Create favorite widget group](actions/create-favorite-widget-groups.md) | POST |  |
| [Delete favorite widget group](actions/delete-favorite-widget-groups-by-id-delete.md) | DELETE |  |
| [Get favorite widgets groups list](actions/list-favorite-widget-groups.md) | GET |  |
| [Update favorite widget's group](actions/update-favorite-widget-groups-by-id-update.md) | PUT |  |

### Favorite Widgets

| Action | Method | Description |
| --- | --- | --- |
| [Add favorite widget](actions/create-favorite-widgets.md) | POST |  |
| [Get favorite widgets list](actions/list-favorite-widgets.md) | GET |  |
| [Rename favorite widget's title](actions/rename-favorite-widgets-by-id-rename.md) | PUT |  |
| [Delete favorite widget](actions/update-favorite-widgets-by-id.md) | PUT |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [File upload](actions/create-vendor-files.md) | POST |  |
| [File upload](actions/create-vendors-files.md) | POST |  |

### Firmware Builds

| Action | Method | Description |
| --- | --- | --- |
| [Request firmware build link user](actions/create-firmware-builds.md) | POST |  |
| [Create firmware build](actions/create-vendor-firmware-builds.md) | POST |  |
| [Delete firmware build](actions/delete-vendor-firmware-builds-by-id-delete.md) | DELETE |  |
| [Show firmware build](actions/get-vendor-firmware-builds-by-id.md) | GET |  |
| [List firware builds](actions/list-vendor-firmware-builds.md) | GET |  |

### Firmware Changelogs

| Action | Method | Description |
| --- | --- | --- |
| [Create firmware changelog](actions/create-vendor-firmware-changelogs.md) | POST |  |
| [Delete firmware changelog](actions/delete-vendor-firmware-changelogs-by-id-delete.md) | DELETE |  |
| [List firware changelogs](actions/list-vendor-firmware-changelogs.md) | GET |  |
| [Update firmware changelog](actions/update-vendor-firmware-changelogs-by-id-update.md) | PUT |  |

### Firmwares

| Action | Method | Description |
| --- | --- | --- |
| [Archive firmware](actions/archive-vendor-firmwares-by-id-archive.md) | DELETE |  |
| [Create firmware](actions/create-vendor-firmwares.md) | POST |  |
| [Delete firmware](actions/delete-vendor-firmwares-by-id-delete.md) | DELETE |  |
| [Show firmware](actions/get-vendor-firmwares-by-id.md) | GET |  |
| [Show firmware](actions/get-vendor-firmwares-by-id-ap.md) | GET |  |
| [List firwares](actions/list-vendor-firmwares.md) | GET |  |
| [Update firmware](actions/update-vendor-firmwares-by-id-ap-update.md) | PUT |  |
| [Update firmware](actions/update-vendor-firmwares-by-id-update.md) | PUT |  |

### Google

| Action | Method | Description |
| --- | --- | --- |
| [Login mobile user with Google](actions/create-sessions-google.md) | POST |  |
| [Login vendor with Google](actions/create-vendor-login-google.md) | POST |  |

### Invite

| Action | Method | Description |
| --- | --- | --- |
| [Create invite share](actions/create-shares-invite.md) | POST |  |

### Layouts

| Action | Method | Description |
| --- | --- | --- |
| [Archive/Unarchive dashboard](actions/archive-vendor-layouts-by-id-archive.md) | DELETE |  |
| [Create layout](actions/create-vendor-layouts.md) | POST |  |
| [Delete layout](actions/delete-vendor-layouts-by-id-delete.md) | DELETE |  |
| [Show layout](actions/get-vendor-layouts-by-id.md) | GET |  |
| [List layouts](actions/list-layouts.md) | GET |  |
| [List layouts](actions/list-vendor-layouts.md) | GET |  |
| [Update layout](actions/update-layouts-by-id-update.md) | PUT |  |
| [Update layout](actions/update-vendor-layouts-by-id-update.md) | PUT |  |

### Link Mobile

| Action | Method | Description |
| --- | --- | --- |
| [Link vendor account to mobile](actions/create-vendor-link-mobile.md) | POST |  |

### Locales

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update locales](actions/bulk-update-vendor-locales-bulk-update.md) | PUT |  |
| [List locales](actions/list-vendor-locales.md) | GET |  |

### Login

| Action | Method | Description |
| --- | --- | --- |
| [Login vendor](actions/create-vendor-login.md) | POST |  |

### Logout

| Action | Method | Description |
| --- | --- | --- |
| [Lougout vendor](actions/create-vendor-logout.md) | POST |  |

### Market

| Action | Method | Description |
| --- | --- | --- |
| [Get market products list](actions/list-market.md) | GET |  |

### Market Devices

| Action | Method | Description |
| --- | --- | --- |
| [Get products list for devices](actions/list-market-devices.md) | GET |  |

### Market Events

| Action | Method | Description |
| --- | --- | --- |
| [Create market event](actions/create-market-events.md) | POST |  |
| [Create market event](actions/create-vendor-market-events.md) | POST |  |

### Mqtt

| Action | Method | Description |
| --- | --- | --- |
| [Get mqtt credentials for user](actions/get-users-mqtt.md) | GET |  |

### Mqtt Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get mqtt credentials for user](actions/create-mqtt-tokens.md) | POST |  |

### Notification Configs

| Action | Method | Description |
| --- | --- | --- |
| [Update notification config](actions/update-notification-configs-by-id-update.md) | PUT |  |

### Notification Records

| Action | Method | Description |
| --- | --- | --- |
| [Delete notification record](actions/delete-notification-records-by-id-delete.md) | DELETE |  |
| [Delete notification record](actions/delete-vendor-notification-records-by-id-delete.md) | DELETE |  |
| [Show notification record](actions/get-notification-records-by-id.md) | GET |  |
| [Show notification record](actions/get-vendor-notification-records-by-id.md) | GET |  |
| [List notification record](actions/list-notification-records.md) | GET |  |
| [List notification record](actions/list-vendor-notification-records.md) | GET |  |
| [Mark notification records as read](actions/mark-read-notification-records-mark-read.md) | PUT |  |
| [Mark notification records as read](actions/mark-read-vendor-notification-records-mark-read.md) | PUT |  |
| [Update notification record](actions/update-notification-records-by-id-update.md) | PUT |  |

### Pairing Config

| Action | Method | Description |
| --- | --- | --- |
| [Create pairing config](actions/create-vendor-pairing-config.md) | POST |  |
| [Show layout](actions/create-vendor-product-by-id-pairing-config.md) | POST |  |
| [Delete pairing config](actions/delete-vendor-pairing-config-by-id-delete.md) | DELETE |  |
| [Update pairing config](actions/update-vendor-pairing-config-by-id.md) | PUT |  |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Create phone number](actions/create-phone-numbers.md) | POST |  |
| [Delete phone number](actions/delete-phone-numbers-by-id-delete.md) | DELETE |  |
| [List phone trigger](actions/list-phone-numbers.md) | GET |  |
| [Update phone trigger](actions/update-phone-numbers-by-id-update.md) | PUT |  |

### Phone Triggers

| Action | Method | Description |
| --- | --- | --- |
| [Check phone trigger](actions/check-phone-triggers-by-id-check.md) | PUT |  |
| [Create phone trigger](actions/create-phone-triggers.md) | POST |  |
| [Delete phone trigger](actions/delete-phone-triggers-by-id-delete.md) | DELETE |  |
| [List phone trigger](actions/list-phone-triggers.md) | GET |  |
| [Update phone trigger](actions/update-phone-triggers-by-id-update.md) | PUT |  |

### Product Versions

| Action | Method | Description |
| --- | --- | --- |
| [Duplicate product version](actions/duplicate-vendor-product-versions-by-id-duplicate.md) | PUT |  |
| [List products versions major](actions/get-vendor-product-versions-major.md) | GET |  |
| [List of product versions](actions/list-product-versions.md) | GET |  |
| [List products](actions/list-vendor-product-versions.md) | GET |  |
| [Update changelogs](actions/update-changelog-vendor-product-versions-by-id-update-changelog.md) | POST |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Archive product](actions/archive-vendor-products-by-id-archive.md) | DELETE |  |
| [Create Product](actions/create-products.md) | POST |  |
| [Create Product](actions/create-vendor-products.md) | POST |  |
| [Delete product](actions/delete-vendor-products-by-id-delete.md) | DELETE |  |
| [Discard product draft](actions/discard-draft-vendor-products-by-id-discard-draft.md) | PUT |  |
| [Approve products](actions/get-admin-products-approve.md) | GET |  |
| [Delete products](actions/get-admin-products-delete.md) | GET |  |
| [Hide products](actions/get-admin-products-hide.md) | GET |  |
| [Unhide products](actions/get-admin-products-unhide.md) | GET |  |
| [Show product](actions/get-products-by-id.md) | GET |  |
| [Show product firmware version](actions/get-products-by-id-firmware-version.md) | GET |  |
| [Show product firmware version](actions/get-public-products-by-id-firmware-version.md) | GET |  |
| [List of product abbreviations](actions/get-vendor-products-abbreviations.md) | GET |  |
| [Approve products](actions/get-vendor-products-approve.md) | GET |  |
| [Show product](actions/get-vendor-products-by-id.md) | GET |  |
| [List products](actions/get-vendor-products-lite.md) | GET |  |
| [List products](actions/list-admin-products.md) | GET |  |
| [List products](actions/list-products.md) | GET |  |
| [List products](actions/list-vendor-products.md) | GET |  |
| [Publish product](actions/publish-vendor-products-by-id-publish.md) | PUT |  |
| [Stage product](actions/stage-vendor-products-by-id-stage.md) | PUT |  |
| [Unstage product](actions/unstage-vendor-products-by-id-unstage.md) | PUT |  |
| [Update product](actions/update-vendor-products-by-id-update.md) | PUT |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get vendor info](actions/create-vendors-profile.md) | POST |  |
| [Profile mobile user](actions/get-users-profile.md) | GET |  |
| [Get vendor info](actions/get-vendor-profile.md) | GET |  |

### References

| Action | Method | Description |
| --- | --- | --- |
| [Reference be name](actions/get-public-references-by-name.md) | GET |  |
| [Reference be name](actions/get-references-by-name.md) | GET |  |
| [Reference be name](actions/get-share-v1-references-by-name.md) | GET |  |
| [All references](actions/list-public-references.md) | GET |  |
| [All references](actions/list-references.md) | GET |  |
| [All references](actions/list-share-v1-references.md) | GET |  |

### Refuse

| Action | Method | Description |
| --- | --- | --- |
| [Refuse products](actions/get-admin-products-refuse.md) | GET |  |

### Register

| Action | Method | Description |
| --- | --- | --- |
| [Register vendor](actions/create-vendor-register.md) | POST |  |

### Reported Issues

| Action | Method | Description |
| --- | --- | --- |
| [Report user issue](actions/create-reported-issues.md) | POST |  |
| [Report vendor issue](actions/create-vendor-reported-issues.md) | POST |  |
| [Set report as solved](actions/solve-admin-reported-issues-solve-by-id.md) | PUT |  |
| [Set report as unsolved](actions/unsolve-admin-reported-issues-unsolve-by-id.md) | PUT |  |

### Request Platform Demo

| Action | Method | Description |
| --- | --- | --- |
| [Request platform demo](actions/create-vendor-request-platform-demo.md) | POST |  |

### Request Reset Password

| Action | Method | Description |
| --- | --- | --- |
| [Request vendor reset password](actions/create-users-request-reset-password.md) | POST |  |
| [Request vendor reset password](actions/create-vendor-request-reset-password.md) | POST |  |

### Reset Password

| Action | Method | Description |
| --- | --- | --- |
| [Reset mobile password](actions/create-users-reset-password.md) | POST |  |
| [Reset vendor password](actions/create-vendor-reset-password.md) | POST |  |

### Schema Versions

| Action | Method | Description |
| --- | --- | --- |
| [All products (in production status) schemas](actions/create-share-v1-schema-versions.md) | POST |  |

### Schemas

| Action | Method | Description |
| --- | --- | --- |
| [All products (in production status) schemas](actions/list-public-schemas.md) | GET |  |
| [All products (in production status) schemas](actions/list-schemas.md) | GET |  |

### Schemas Versions

| Action | Method | Description |
| --- | --- | --- |
| [All products (in production status) schemas with each major latest versions](actions/create-public-schemas-versions.md) | POST |  |
| [All products (in production status) schemas](actions/create-schemas-versions.md) | POST |  |
| [All products (in production status) schemas with each major latest versions](actions/list-public-schemas-versions.md) | GET |  |
| [All products (in production status) schemas](actions/list-schemas-versions.md) | GET |  |

### Selected Widgets

| Action | Method | Description |
| --- | --- | --- |
| [Add selected widget](actions/create-selected-widgets.md) | POST |  |
| [Show selected widget](actions/get-selected-widgets-by-id.md) | GET |  |
| [Get selected widgets list](actions/list-selected-widgets.md) | GET |  |

### Sensors Info

| Action | Method | Description |
| --- | --- | --- |
| [Sensor info create](actions/create-vendor-sensors-info.md) | POST |  |
| [Delete sensor info](actions/delete-vendor-sensors-info-delete.md) | DELETE |  |
| [List sensors info](actions/list-vendor-sensors-info.md) | GET |  |
| [Sensor info update](actions/update-vendor-sensors-info-update.md) | PUT |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Login mobile user](actions/create-sessions.md) | POST |  |

### Share Link Devices

| Action | Method | Description |
| --- | --- | --- |
| [Delete shared device](actions/delete-share-link-devices-by-id-delete.md) | DELETE |  |
| [List shared devices](actions/list-share-link-devices.md) | GET |  |
| [Update shared device](actions/update-share-link-devices-by-id-update.md) | PUT |  |

### Share Links

| Action | Method | Description |
| --- | --- | --- |
| [Create share link](actions/create-share-links.md) | POST |  |
| [Delete share link](actions/delete-share-links-by-id-delete.md) | DELETE |  |
| [Show share link](actions/get-share-links-by-id.md) | GET |  |
| [Show share-link](actions/get-share-v1-link.md) | GET |  |
| [Show share-link](actions/get-share-v1-short-link-by-id.md) | GET |  |
| [List share links](actions/list-share-links.md) | GET |  |
| [Update share link](actions/update-share-links-by-id-update.md) | PUT |  |

### Shared Devices

| Action | Method | Description |
| --- | --- | --- |
| [Delete shared device](actions/delete-shared-devices-by-id-delete.md) | DELETE |  |
| [List shared devices](actions/list-shared-devices.md) | GET |  |
| [Update shared device](actions/update-shared-devices-by-id-update.md) | PUT |  |

### Shares

| Action | Method | Description |
| --- | --- | --- |
| [Create share](actions/create-shares.md) | POST |  |
| [Delete share](actions/delete-shares-by-id-delete.md) | DELETE |  |
| [List shares](actions/list-shares.md) | GET |  |
| [Unhide share](actions/unhide-shares-by-id-unhide.md) | PUT |  |
| [Update share](actions/update-shares-by-id-update.md) | PUT |  |

### Slack Webhooks

| Action | Method | Description |
| --- | --- | --- |
| [Add slack webhook](actions/create-slack-webhooks.md) | POST |  |
| [Delete slack webhook](actions/delete-slack-webhooks-by-id-delete.md) | DELETE |  |
| [Get slack webhooks list](actions/list-slack-webhooks.md) | GET |  |
| [Update slack webhook](actions/update-slack-webhooks-by-id-update.md) | PUT |  |

### Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Bar statistics](actions/get-vendor-statistics-bar.md) | GET |  |
| [List statistics intervals](actions/get-vendor-statistics-intervals.md) | GET |  |
| [Pie statistics](actions/get-vendor-statistics-pie.md) | GET |  |
| [Pie statistics](actions/get-vendor-statistics-version-progress.md) | GET |  |
| [List statistics versions](actions/get-vendor-statistics-versions.md) | GET |  |
| [List statistics](actions/list-vendor-statistics.md) | GET |  |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [User survey](actions/create-vendor-survey.md) | POST |  |

### Telegram Chat Ids

| Action | Method | Description |
| --- | --- | --- |
| [Add telegram chat_id](actions/create-telegram-chat-ids.md) | POST |  |
| [Delete telegram chat id](actions/delete-telegram-chat-ids-by-id-delete.md) | DELETE |  |
| [Get telegram chat ids list](actions/list-telegram-chat-ids.md) | GET |  |
| [Update telegram chats's info](actions/update-telegram-chat-ids-by-id-update.md) | PUT |  |

### Timelines

| Action | Method | Description |
| --- | --- | --- |
| [List share timelines number](actions/get-share-v1-timelines-number.md) | GET |  |
| [List share timelines string](actions/get-share-v1-timelines-string.md) | GET |  |
| [List timelines number](actions/get-timelines-number.md) | GET |  |
| [List timelines string](actions/get-timelines-string.md) | GET |  |
| [List timelines number](actions/get-vendor-timelines-number.md) | GET |  |
| [List timelines string](actions/get-vendor-timelines-string.md) | GET |  |
| [List timelines](actions/list-share-v1-timelines.md) | GET |  |
| [List timelines](actions/list-timelines.md) | GET |  |
| [List timelines](actions/list-vendor-timelines.md) | GET |  |

### Topics

| Action | Method | Description |
| --- | --- | --- |
| [List share](actions/list-shares-topics.md) | GET |  |

### Translate

| Action | Method | Description |
| --- | --- | --- |
| [Translate widget values](actions/translate-vendor-translate.md) | PUT |  |

### Update

| Action | Method | Description |
| --- | --- | --- |
| [Update vendor](actions/update-vendor-update.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Register mobile user](actions/create-users.md) | POST |  |
| [Update mobile user](actions/update-users-update.md) | PUT |  |

### Validate Reset Password Code

| Action | Method | Description |
| --- | --- | --- |
| [Validate reset password code](actions/create-users-validate-reset-password-code.md) | POST |  |

### Verify

| Action | Method | Description |
| --- | --- | --- |
| [Verify share emails](actions/create-shares-verify.md) | POST |  |

### Version Intervals

| Action | Method | Description |
| --- | --- | --- |
| [List statistics intervals](actions/list-vendor-statistics-version-intervals.md) | GET |  |

### Whatsapp Chat Ids

| Action | Method | Description |
| --- | --- | --- |
| [Add WhatsApp chat_id](actions/create-whatsapp-chat-ids.md) | POST |  |
| [Delete WhatsApp chat id](actions/delete-whatsapp-chat-ids-by-id-delete.md) | DELETE |  |
| [Get WhatsApp chat ids list](actions/list-whatsapp-chat-ids.md) | GET |  |
| [Update WhatsApp chats's info](actions/update-whatsapp-chat-ids-by-id-update.md) | PUT |  |

