# 2Smart Cloud: Native API Reference

A consolidated summary of 2Smart Cloud's API configuration and 235 documented operations, with links to official documentation.

- **Official docs:** https://cloud.2smart.com/swagger/
- **OpenAPI specification:** https://cloud.2smart.com/swagger/apidoc.yaml
- **API base URL:** `https://cloud.2smart.com/robot/v1`

## Authentication

### Basic Auth

Use the 2Smart Cloud vendor API token as the username and the secret token as the password for HTTP Basic authentication.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://cloud.2smart.com/swagger/)

## Endpoints (235 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive/Unarchive layout](actions/archive-vendor-dashboards-by-id-archive.md) | `POST /vendor/dashboards/{id}/archive` | [docs](https://cloud.2smart.com/swagger/) |
| [Archive firmware](actions/archive-vendor-firmwares-by-id-archive.md) | `POST /vendor/firmwares/{id}/archive` | [docs](https://cloud.2smart.com/swagger/) |
| [Archive/Unarchive dashboard](actions/archive-vendor-layouts-by-id-archive.md) | `POST /vendor/layouts/{id}/archive` | [docs](https://cloud.2smart.com/swagger/) |
| [Archive product](actions/archive-vendor-products-by-id-archive.md) | `POST /vendor/products/{id}/archive` | [docs](https://cloud.2smart.com/swagger/) |
| [Bulk update favorite widgets groups positions](actions/bulk-update-favorite-widget-groups-bulk-update.md) | `POST /favorite-widget-groups/bulk-update` | [docs](https://cloud.2smart.com/swagger/) |
| [Bulk Update locales](actions/bulk-update-vendor-locales-bulk-update.md) | `POST /vendor/locales/bulk-update` | [docs](https://cloud.2smart.com/swagger/) |
| [Check phone trigger](actions/check-phone-triggers-by-id-check.md) | `POST /phone-triggers/{id}/check` | [docs](https://cloud.2smart.com/swagger/) |
| [Check if there is biometric keys for this device](actions/create-devices-by-device-id-check-biometric.md) | `POST /devices/{device_id}/check-biometric` | [docs](https://cloud.2smart.com/swagger/) |
| [Create favorite widget group](actions/create-devices-by-device-id-credentials.md) | `POST /devices/{device_id}/credentials` | [docs](https://cloud.2smart.com/swagger/) |
| [Create favorite widget group](actions/create-favorite-widget-groups.md) | `POST /favorite-widget-groups` | [docs](https://cloud.2smart.com/swagger/) |
| [Bulk add favorite widgets to groups](actions/create-favorite-widget-groups-bulk-add.md) | `POST /favorite-widget-groups/bulk-add` | [docs](https://cloud.2smart.com/swagger/) |
| [Add favorite widget](actions/create-favorite-widgets.md) | `POST /favorite-widgets` | [docs](https://cloud.2smart.com/swagger/) |
| [Bulk delete favorite widgets](actions/create-favorite-widgets-bulk-delete.md) | `POST /favorite-widgets/bulk-delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Request firmware build link user](actions/create-firmware-builds.md) | `POST /firmware-builds` | [docs](https://cloud.2smart.com/swagger/) |
| [Send `contact us` email](actions/create-landing-emails-contact-us.md) | `POST /landing/emails/contact-us` | [docs](https://cloud.2smart.com/swagger/) |
| [Create market event](actions/create-market-events.md) | `POST /market-events` | [docs](https://cloud.2smart.com/swagger/) |
| [Get mqtt credentials for user](actions/create-mqtt-tokens.md) | `POST /mqtt-tokens` | [docs](https://cloud.2smart.com/swagger/) |
| [Create phone number](actions/create-phone-numbers.md) | `POST /phone-numbers` | [docs](https://cloud.2smart.com/swagger/) |
| [Create phone number](actions/create-phone-numbers-bulk.md) | `POST /phone-numbers/bulk` | [docs](https://cloud.2smart.com/swagger/) |
| [Create phone trigger](actions/create-phone-triggers.md) | `POST /phone-triggers` | [docs](https://cloud.2smart.com/swagger/) |
| [Create Product](actions/create-products.md) | `POST /products` | [docs](https://cloud.2smart.com/swagger/) |
| [All products (in production status) schemas with each major latest versions](actions/create-public-schemas-versions.md) | `POST /public/schemas-versions` | [docs](https://cloud.2smart.com/swagger/) |
| [Report user issue](actions/create-reported-issues.md) | `POST /reported-issues` | [docs](https://cloud.2smart.com/swagger/) |
| [All products (in production status) schemas](actions/create-schemas-versions.md) | `POST /schemas-versions` | [docs](https://cloud.2smart.com/swagger/) |
| [Add selected widget](actions/create-selected-widgets.md) | `POST /selected-widgets` | [docs](https://cloud.2smart.com/swagger/) |
| [Login mobile user](actions/create-sessions.md) | `POST /sessions` | [docs](https://cloud.2smart.com/swagger/) |
| [Login mobile user with Apple](actions/create-sessions-apple.md) | `POST /sessions/apple` | [docs](https://cloud.2smart.com/swagger/) |
| [Login mobile user with biometric key](actions/create-sessions-biometric.md) | `POST /sessions/biometric` | [docs](https://cloud.2smart.com/swagger/) |
| [Login mobile user with Facebook](actions/create-sessions-facebook.md) | `POST /sessions/facebook` | [docs](https://cloud.2smart.com/swagger/) |
| [Login mobile user with Google](actions/create-sessions-google.md) | `POST /sessions/google` | [docs](https://cloud.2smart.com/swagger/) |
| [Bulk Delete shared device](actions/create-share-link-devices-bulk-delete.md) | `POST /share-link-devices/bulk-delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Create share link](actions/create-share-links.md) | `POST /share-links` | [docs](https://cloud.2smart.com/swagger/) |
| [All products (in production status) schemas](actions/create-share-v1-schema-versions.md) | `POST /share/v1/schema-versions` | [docs](https://cloud.2smart.com/swagger/) |
| [Bulk Delete shared device](actions/create-shared-devices-bulk-delete.md) | `POST /shared-devices/bulk-delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Create share](actions/create-shares.md) | `POST /shares` | [docs](https://cloud.2smart.com/swagger/) |
| [Create invite share](actions/create-shares-invite.md) | `POST /shares/invite` | [docs](https://cloud.2smart.com/swagger/) |
| [Verify share emails](actions/create-shares-verify.md) | `POST /shares/verify` | [docs](https://cloud.2smart.com/swagger/) |
| [Add slack webhook](actions/create-slack-webhooks.md) | `POST /slack-webhooks` | [docs](https://cloud.2smart.com/swagger/) |
| [Add telegram chat_id](actions/create-telegram-chat-ids.md) | `POST /telegram-chat_ids` | [docs](https://cloud.2smart.com/swagger/) |
| [Register mobile user](actions/create-users.md) | `POST /users` | [docs](https://cloud.2smart.com/swagger/) |
| [Change password mobile user](actions/create-users-change-password.md) | `POST /users/change-password` | [docs](https://cloud.2smart.com/swagger/) |
| [Clear phone number of mobile user](actions/create-users-clear-phone-number.md) | `POST /users/clear-phone-number` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete biometric key for device](actions/create-users-delete-biometric.md) | `POST /users/delete/biometric` | [docs](https://cloud.2smart.com/swagger/) |
| [Request vendor reset password](actions/create-users-request-reset-password.md) | `POST /users/request-reset-password` | [docs](https://cloud.2smart.com/swagger/) |
| [Reset mobile password](actions/create-users-reset-password.md) | `POST /users/reset-password` | [docs](https://cloud.2smart.com/swagger/) |
| [Update mobile user with biometric](actions/create-users-update-biometric.md) | `POST /users/update/biometric` | [docs](https://cloud.2smart.com/swagger/) |
| [Validate reset password code](actions/create-users-validate-reset-password-code.md) | `POST /users/validate-reset-password-code` | [docs](https://cloud.2smart.com/swagger/) |
| [Create api token](actions/create-vendor-api-tokens.md) | `POST /vendor/api-tokens` | [docs](https://cloud.2smart.com/swagger/) |
| [Binary upload](actions/create-vendor-binaries.md) | `POST /vendor/binaries` | [docs](https://cloud.2smart.com/swagger/) |
| [Binary mock upload](actions/create-vendor-binaries-mock.md) | `POST /vendor/binaries-mock` | [docs](https://cloud.2smart.com/swagger/) |
| [Create build part](actions/create-vendor-build-parts.md) | `POST /vendor/build-parts` | [docs](https://cloud.2smart.com/swagger/) |
| [Build upload](actions/create-vendor-builds.md) | `POST /vendor/builds` | [docs](https://cloud.2smart.com/swagger/) |
| [Update vendor](actions/create-vendor-change-password.md) | `POST /vendor/change-password` | [docs](https://cloud.2smart.com/swagger/) |
| [Check reset vendor password token](actions/create-vendor-check-reset-password-token.md) | `POST /vendor/check-reset-password-token` | [docs](https://cloud.2smart.com/swagger/) |
| [Create dashboard](actions/create-vendor-dashboards.md) | `POST /vendor/dashboards` | [docs](https://cloud.2smart.com/swagger/) |
| [File upload](actions/create-vendor-files.md) | `POST /vendor/files` | [docs](https://cloud.2smart.com/swagger/) |
| [Create firmware build](actions/create-vendor-firmware-builds.md) | `POST /vendor/firmware-builds` | [docs](https://cloud.2smart.com/swagger/) |
| [Create firmware changelog](actions/create-vendor-firmware-changelogs.md) | `POST /vendor/firmware-changelogs` | [docs](https://cloud.2smart.com/swagger/) |
| [Create firmware](actions/create-vendor-firmwares.md) | `POST /vendor/firmwares` | [docs](https://cloud.2smart.com/swagger/) |
| [Create layout](actions/create-vendor-layouts.md) | `POST /vendor/layouts` | [docs](https://cloud.2smart.com/swagger/) |
| [Link vendor account to mobile](actions/create-vendor-link-mobile.md) | `POST /vendor/link-mobile` | [docs](https://cloud.2smart.com/swagger/) |
| [Login vendor](actions/create-vendor-login.md) | `POST /vendor/login` | [docs](https://cloud.2smart.com/swagger/) |
| [Login vendor with Apple](actions/create-vendor-login-apple.md) | `POST /vendor/login/apple` | [docs](https://cloud.2smart.com/swagger/) |
| [Login vendor with Facebook](actions/create-vendor-login-facebook.md) | `POST /vendor/login/facebook` | [docs](https://cloud.2smart.com/swagger/) |
| [Login vendor with Google](actions/create-vendor-login-google.md) | `POST /vendor/login/google` | [docs](https://cloud.2smart.com/swagger/) |
| [Lougout vendor](actions/create-vendor-logout.md) | `POST /vendor/logout` | [docs](https://cloud.2smart.com/swagger/) |
| [Create market event](actions/create-vendor-market-events.md) | `POST /vendor/market-events` | [docs](https://cloud.2smart.com/swagger/) |
| [Create pairing config](actions/create-vendor-pairing-config.md) | `POST /vendor/pairing-config` | [docs](https://cloud.2smart.com/swagger/) |
| [Show layout](actions/create-vendor-product-by-id-pairing-config.md) | `POST /vendor/product/{id}/pairing-config` | [docs](https://cloud.2smart.com/swagger/) |
| [Create Product](actions/create-vendor-products.md) | `POST /vendor/products` | [docs](https://cloud.2smart.com/swagger/) |
| [Register vendor](actions/create-vendor-register.md) | `POST /vendor/register` | [docs](https://cloud.2smart.com/swagger/) |
| [Report vendor issue](actions/create-vendor-reported-issues.md) | `POST /vendor/reported-issues` | [docs](https://cloud.2smart.com/swagger/) |
| [Request platform demo](actions/create-vendor-request-platform-demo.md) | `POST /vendor/request-platform-demo` | [docs](https://cloud.2smart.com/swagger/) |
| [Request vendor reset password](actions/create-vendor-request-reset-password.md) | `POST /vendor/request-reset-password` | [docs](https://cloud.2smart.com/swagger/) |
| [Reset vendor password](actions/create-vendor-reset-password.md) | `POST /vendor/reset-password` | [docs](https://cloud.2smart.com/swagger/) |
| [Sensor info create](actions/create-vendor-sensors-info.md) | `POST /vendor/sensors-info` | [docs](https://cloud.2smart.com/swagger/) |
| [User survey](actions/create-vendor-survey.md) | `POST /vendor/survey` | [docs](https://cloud.2smart.com/swagger/) |
| [File upload](actions/create-vendors-files.md) | `POST /vendors/files` | [docs](https://cloud.2smart.com/swagger/) |
| [Get vendor info](actions/create-vendors-profile.md) | `POST /vendors/profile` | [docs](https://cloud.2smart.com/swagger/) |
| [Add WhatsApp chat_id](actions/create-whatsapp-chat-ids.md) | `POST /whatsapp-chat_ids` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete favorite widget group](actions/delete-favorite-widget-groups-by-id-delete.md) | `POST /favorite-widget-groups/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete notification record](actions/delete-notification-records-by-id-delete.md) | `POST /notification-records/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete phone number](actions/delete-phone-numbers-by-id-delete.md) | `POST /phone-numbers/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete phone trigger](actions/delete-phone-triggers-by-id-delete.md) | `POST /phone-triggers/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete shared device](actions/delete-share-link-devices-by-id-delete.md) | `POST /share-link-devices/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete share link](actions/delete-share-links-by-id-delete.md) | `POST /share-links/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete shared device](actions/delete-shared-devices-by-id-delete.md) | `POST /shared-devices/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete share](actions/delete-shares-by-id-delete.md) | `POST /shares/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete slack webhook](actions/delete-slack-webhooks-by-id-delete.md) | `POST /slack-webhooks/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete telegram chat id](actions/delete-telegram-chat-ids-by-id-delete.md) | `POST /telegram-chat_ids/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete api token](actions/delete-vendor-api-tokens-by-id-delete.md) | `POST /vendor/api-tokens/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete build part](actions/delete-vendor-build-parts-by-id-delete.md) | `POST /vendor/build-parts/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete dashboard](actions/delete-vendor-dashboards-by-id-delete.md) | `POST /vendor/dashboards/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete firmware build](actions/delete-vendor-firmware-builds-by-id-delete.md) | `POST /vendor/firmware-builds/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete firmware changelog](actions/delete-vendor-firmware-changelogs-by-id-delete.md) | `POST /vendor/firmware-changelogs/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete firmware](actions/delete-vendor-firmwares-by-id-delete.md) | `POST /vendor/firmwares/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete layout](actions/delete-vendor-layouts-by-id-delete.md) | `POST /vendor/layouts/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete notification record](actions/delete-vendor-notification-records-by-id-delete.md) | `POST /vendor/notification-records/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete pairing config](actions/delete-vendor-pairing-config-by-id-delete.md) | `POST /vendor/pairing-config/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete product](actions/delete-vendor-products-by-id-delete.md) | `POST /vendor/products/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete sensor info](actions/delete-vendor-sensors-info-delete.md) | `POST /vendor/sensors-info/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete WhatsApp chat id](actions/delete-whatsapp-chat-ids-by-id-delete.md) | `POST /whatsapp-chat_ids/{id}/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Discard product draft](actions/discard-draft-vendor-products-by-id-discard-draft.md) | `POST /vendor/products/{id}/discard-draft` | [docs](https://cloud.2smart.com/swagger/) |
| [Duplicate product version](actions/duplicate-vendor-product-versions-by-id-duplicate.md) | `POST /vendor/product-versions/{id}/duplicate` | [docs](https://cloud.2smart.com/swagger/) |
| [Update build part](actions/factory-vendor-build-parts-by-id-factory.md) | `POST /vendor/build-parts/{id}/factory` | [docs](https://cloud.2smart.com/swagger/) |
| [Aggregated value for topic](actions/get-admin-aggregated-value.md) | `GET /admin/aggregated-value` | [docs](https://cloud.2smart.com/swagger/) |
| [Approve products](actions/get-admin-products-approve.md) | `GET /admin/products/approve` | [docs](https://cloud.2smart.com/swagger/) |
| [Clear products abbreviations](actions/get-admin-products-clear-abbreviations.md) | `GET /admin/products/clear-abbreviations` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete products](actions/get-admin-products-delete.md) | `GET /admin/products/delete` | [docs](https://cloud.2smart.com/swagger/) |
| [Hide products](actions/get-admin-products-hide.md) | `GET /admin/products/hide` | [docs](https://cloud.2smart.com/swagger/) |
| [Refuse products](actions/get-admin-products-refuse.md) | `GET /admin/products/refuse` | [docs](https://cloud.2smart.com/swagger/) |
| [Unhide products](actions/get-admin-products-unhide.md) | `GET /admin/products/unhide` | [docs](https://cloud.2smart.com/swagger/) |
| [Show notification record](actions/get-notification-records-by-id.md) | `GET /notification-records/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Show product](actions/get-products-by-id.md) | `GET /products/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Show product firmware version](actions/get-products-by-id-firmware-version.md) | `GET /products/{id}/firmware-version` | [docs](https://cloud.2smart.com/swagger/) |
| [Show product firmware version](actions/get-public-products-by-id-firmware-version.md) | `GET /public/products/{id}/firmware-version` | [docs](https://cloud.2smart.com/swagger/) |
| [Reference be name](actions/get-public-references-by-name.md) | `GET /public/references/{name}` | [docs](https://cloud.2smart.com/swagger/) |
| [Reference be name](actions/get-references-by-name.md) | `GET /references/{name}` | [docs](https://cloud.2smart.com/swagger/) |
| [Show selected widget](actions/get-selected-widgets-by-id.md) | `GET /selected-widgets/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Show share link](actions/get-share-links-by-id.md) | `GET /share-links/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Aggregated value for topic](actions/get-share-v1-aggregated-value.md) | `GET /share/v1/aggregated-value` | [docs](https://cloud.2smart.com/swagger/) |
| [Show share-link](actions/get-share-v1-link.md) | `GET /share/v1/link` | [docs](https://cloud.2smart.com/swagger/) |
| [Reference be name](actions/get-share-v1-references-by-name.md) | `GET /share/v1/references/{name}` | [docs](https://cloud.2smart.com/swagger/) |
| [Show share-link](actions/get-share-v1-short-link-by-id.md) | `GET /share/v1/short-link/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [List share timelines number](actions/get-share-v1-timelines-number.md) | `GET /share/v1/timelines/number` | [docs](https://cloud.2smart.com/swagger/) |
| [List share timelines string](actions/get-share-v1-timelines-string.md) | `GET /share/v1/timelines/string` | [docs](https://cloud.2smart.com/swagger/) |
| [List timelines](actions/get-timelines-aggregated-value.md) | `GET /timelines/aggregated-value` | [docs](https://cloud.2smart.com/swagger/) |
| [List timelines number](actions/get-timelines-number.md) | `GET /timelines/number` | [docs](https://cloud.2smart.com/swagger/) |
| [List timelines string](actions/get-timelines-string.md) | `GET /timelines/string` | [docs](https://cloud.2smart.com/swagger/) |
| [Register mobile user](actions/get-users-check-exists.md) | `GET /users/check-exists` | [docs](https://cloud.2smart.com/swagger/) |
| [Get mqtt credentials for user](actions/get-users-mqtt.md) | `GET /users/mqtt` | [docs](https://cloud.2smart.com/swagger/) |
| [Profile mobile user](actions/get-users-profile.md) | `GET /users/profile` | [docs](https://cloud.2smart.com/swagger/) |
| [Show api token](actions/get-vendor-api-tokens-by-id.md) | `GET /vendor/api-tokens/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Show dashboard](actions/get-vendor-dashboards-by-id.md) | `GET /vendor/dashboards/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Show firmware build](actions/get-vendor-firmware-builds-by-id.md) | `GET /vendor/firmware-builds/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Show firmware](actions/get-vendor-firmwares-by-id.md) | `GET /vendor/firmwares/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Show firmware](actions/get-vendor-firmwares-by-id-ap.md) | `GET /vendor/firmwares/{id}/ap` | [docs](https://cloud.2smart.com/swagger/) |
| [Show layout](actions/get-vendor-layouts-by-id.md) | `GET /vendor/layouts/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Show notification record](actions/get-vendor-notification-records-by-id.md) | `GET /vendor/notification-records/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [List products versions major](actions/get-vendor-product-versions-major.md) | `GET /vendor/product-versions/major` | [docs](https://cloud.2smart.com/swagger/) |
| [List of product abbreviations](actions/get-vendor-products-abbreviations.md) | `GET /vendor/products/abbreviations` | [docs](https://cloud.2smart.com/swagger/) |
| [Approve products](actions/get-vendor-products-approve.md) | `GET /vendor/products/approve` | [docs](https://cloud.2smart.com/swagger/) |
| [Show product](actions/get-vendor-products-by-id.md) | `GET /vendor/products/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [List products](actions/get-vendor-products-lite.md) | `GET /vendor/products/lite` | [docs](https://cloud.2smart.com/swagger/) |
| [Get vendor info](actions/get-vendor-profile.md) | `GET /vendor/profile` | [docs](https://cloud.2smart.com/swagger/) |
| [Bar statistics](actions/get-vendor-statistics-bar.md) | `GET /vendor/statistics/bar` | [docs](https://cloud.2smart.com/swagger/) |
| [List statistics intervals](actions/get-vendor-statistics-intervals.md) | `GET /vendor/statistics/intervals` | [docs](https://cloud.2smart.com/swagger/) |
| [Pie statistics](actions/get-vendor-statistics-pie.md) | `GET /vendor/statistics/pie` | [docs](https://cloud.2smart.com/swagger/) |
| [Pie statistics](actions/get-vendor-statistics-version-progress.md) | `GET /vendor/statistics/version-progress` | [docs](https://cloud.2smart.com/swagger/) |
| [List statistics versions](actions/get-vendor-statistics-versions.md) | `GET /vendor/statistics/versions` | [docs](https://cloud.2smart.com/swagger/) |
| [List timelines number](actions/get-vendor-timelines-number.md) | `GET /vendor/timelines/number` | [docs](https://cloud.2smart.com/swagger/) |
| [List timelines string](actions/get-vendor-timelines-string.md) | `GET /vendor/timelines/string` | [docs](https://cloud.2smart.com/swagger/) |
| [List devices](actions/list-admin-devices.md) | `GET /admin/devices` | [docs](https://cloud.2smart.com/swagger/) |
| [List products](actions/list-admin-products.md) | `GET /admin/products` | [docs](https://cloud.2smart.com/swagger/) |
| [Get CSRF Token](actions/list-csrf-token.md) | `GET /csrf_token` | [docs](https://cloud.2smart.com/swagger/) |
| [Get favorite widgets groups list](actions/list-favorite-widget-groups.md) | `GET /favorite-widget-groups` | [docs](https://cloud.2smart.com/swagger/) |
| [Get favorite widgets list](actions/list-favorite-widgets.md) | `GET /favorite-widgets` | [docs](https://cloud.2smart.com/swagger/) |
| [List layouts](actions/list-layouts.md) | `GET /layouts` | [docs](https://cloud.2smart.com/swagger/) |
| [Get market products list](actions/list-market.md) | `GET /market` | [docs](https://cloud.2smart.com/swagger/) |
| [Get products list for devices](actions/list-market-devices.md) | `GET /market-devices` | [docs](https://cloud.2smart.com/swagger/) |
| [List notification record](actions/list-notification-records.md) | `GET /notification-records` | [docs](https://cloud.2smart.com/swagger/) |
| [List phone trigger](actions/list-phone-numbers.md) | `GET /phone-numbers` | [docs](https://cloud.2smart.com/swagger/) |
| [List phone trigger](actions/list-phone-triggers.md) | `GET /phone-triggers` | [docs](https://cloud.2smart.com/swagger/) |
| [List of product versions](actions/list-product-versions.md) | `GET /product-versions` | [docs](https://cloud.2smart.com/swagger/) |
| [List products](actions/list-products.md) | `GET /products` | [docs](https://cloud.2smart.com/swagger/) |
| [All references](actions/list-public-references.md) | `GET /public/references` | [docs](https://cloud.2smart.com/swagger/) |
| [All products (in production status) schemas](actions/list-public-schemas.md) | `GET /public/schemas` | [docs](https://cloud.2smart.com/swagger/) |
| [All products (in production status) schemas with each major latest versions](actions/list-public-schemas-versions.md) | `GET /public/schemas-versions` | [docs](https://cloud.2smart.com/swagger/) |
| [All references](actions/list-references.md) | `GET /references` | [docs](https://cloud.2smart.com/swagger/) |
| [All products (in production status) schemas](actions/list-schemas.md) | `GET /schemas` | [docs](https://cloud.2smart.com/swagger/) |
| [All products (in production status) schemas](actions/list-schemas-versions.md) | `GET /schemas-versions` | [docs](https://cloud.2smart.com/swagger/) |
| [Get selected widgets list](actions/list-selected-widgets.md) | `GET /selected-widgets` | [docs](https://cloud.2smart.com/swagger/) |
| [List shared devices](actions/list-share-link-devices.md) | `GET /share-link-devices` | [docs](https://cloud.2smart.com/swagger/) |
| [List share links](actions/list-share-links.md) | `GET /share-links` | [docs](https://cloud.2smart.com/swagger/) |
| [All references](actions/list-share-v1-references.md) | `GET /share/v1/references` | [docs](https://cloud.2smart.com/swagger/) |
| [List timelines](actions/list-share-v1-timelines.md) | `GET /share/v1/timelines` | [docs](https://cloud.2smart.com/swagger/) |
| [List shared devices](actions/list-shared-devices.md) | `GET /shared-devices` | [docs](https://cloud.2smart.com/swagger/) |
| [List shares](actions/list-shares.md) | `GET /shares` | [docs](https://cloud.2smart.com/swagger/) |
| [List share](actions/list-shares-topics.md) | `GET /shares/topics` | [docs](https://cloud.2smart.com/swagger/) |
| [Get slack webhooks list](actions/list-slack-webhooks.md) | `GET /slack-webhooks` | [docs](https://cloud.2smart.com/swagger/) |
| [Get telegram chat ids list](actions/list-telegram-chat-ids.md) | `GET /telegram-chat_ids` | [docs](https://cloud.2smart.com/swagger/) |
| [List timelines](actions/list-timelines.md) | `GET /timelines` | [docs](https://cloud.2smart.com/swagger/) |
| [Check if user has biometric key](actions/list-users-check-biometric.md) | `GET /users/check/biometric` | [docs](https://cloud.2smart.com/swagger/) |
| [List api tokens](actions/list-vendor-api-tokens.md) | `GET /vendor/api-tokens` | [docs](https://cloud.2smart.com/swagger/) |
| [List dashboards](actions/list-vendor-dashboards.md) | `GET /vendor/dashboards` | [docs](https://cloud.2smart.com/swagger/) |
| [List firware builds](actions/list-vendor-firmware-builds.md) | `GET /vendor/firmware-builds` | [docs](https://cloud.2smart.com/swagger/) |
| [List firware changelogs](actions/list-vendor-firmware-changelogs.md) | `GET /vendor/firmware-changelogs` | [docs](https://cloud.2smart.com/swagger/) |
| [List firwares](actions/list-vendor-firmwares.md) | `GET /vendor/firmwares` | [docs](https://cloud.2smart.com/swagger/) |
| [List layouts](actions/list-vendor-layouts.md) | `GET /vendor/layouts` | [docs](https://cloud.2smart.com/swagger/) |
| [List locales](actions/list-vendor-locales.md) | `GET /vendor/locales` | [docs](https://cloud.2smart.com/swagger/) |
| [List notification record](actions/list-vendor-notification-records.md) | `GET /vendor/notification-records` | [docs](https://cloud.2smart.com/swagger/) |
| [List products](actions/list-vendor-product-versions.md) | `GET /vendor/product-versions` | [docs](https://cloud.2smart.com/swagger/) |
| [List products](actions/list-vendor-products.md) | `GET /vendor/products` | [docs](https://cloud.2smart.com/swagger/) |
| [List sensors info](actions/list-vendor-sensors-info.md) | `GET /vendor/sensors-info` | [docs](https://cloud.2smart.com/swagger/) |
| [List statistics](actions/list-vendor-statistics.md) | `GET /vendor/statistics` | [docs](https://cloud.2smart.com/swagger/) |
| [List statistics intervals](actions/list-vendor-statistics-version-intervals.md) | `GET /vendor/statistics/version-intervals` | [docs](https://cloud.2smart.com/swagger/) |
| [List timelines](actions/list-vendor-timelines.md) | `GET /vendor/timelines` | [docs](https://cloud.2smart.com/swagger/) |
| [Get WhatsApp chat ids list](actions/list-whatsapp-chat-ids.md) | `GET /whatsapp-chat_ids` | [docs](https://cloud.2smart.com/swagger/) |
| [Mark notification records as read](actions/mark-read-notification-records-mark-read.md) | `POST /notification-records/mark-read` | [docs](https://cloud.2smart.com/swagger/) |
| [Mark notification records as read](actions/mark-read-vendor-notification-records-mark-read.md) | `POST /vendor/notification-records/mark-read` | [docs](https://cloud.2smart.com/swagger/) |
| [Publish product](actions/publish-vendor-products-by-id-publish.md) | `POST /vendor/products/{id}/publish` | [docs](https://cloud.2smart.com/swagger/) |
| [Rename favorite widget's title](actions/rename-favorite-widgets-by-id-rename.md) | `POST /favorite-widgets/{id}/rename` | [docs](https://cloud.2smart.com/swagger/) |
| [Set report as solved](actions/solve-admin-reported-issues-solve-by-id.md) | `POST /admin/reported-issues/solve/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Stage product](actions/stage-vendor-products-by-id-stage.md) | `POST /vendor/products/{id}/stage` | [docs](https://cloud.2smart.com/swagger/) |
| [Translate widget values](actions/translate-vendor-translate.md) | `POST /vendor/translate` | [docs](https://cloud.2smart.com/swagger/) |
| [Unhide share](actions/unhide-shares-by-id-unhide.md) | `POST /shares/{id}/unhide` | [docs](https://cloud.2smart.com/swagger/) |
| [Set report as unsolved](actions/unsolve-admin-reported-issues-unsolve-by-id.md) | `POST /admin/reported-issues/unsolve/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Unstage product](actions/unstage-vendor-products-by-id-unstage.md) | `POST /vendor/products/{id}/unstage` | [docs](https://cloud.2smart.com/swagger/) |
| [Update changelogs](actions/update-changelog-vendor-product-versions-by-id-update-changelog.md) | `POST /vendor/product-versions/{id}/update-changelog` | [docs](https://cloud.2smart.com/swagger/) |
| [Update favorite widget's group](actions/update-favorite-widget-groups-by-id-update.md) | `POST /favorite-widget-groups/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Delete favorite widget](actions/update-favorite-widgets-by-id.md) | `DELETE /favorite-widgets/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Update layout](actions/update-layouts-by-id-update.md) | `POST /layouts/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update notification config](actions/update-notification-configs-by-id-update.md) | `POST /notification-configs/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update notification record](actions/update-notification-records-by-id-update.md) | `POST /notification-records/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update phone trigger](actions/update-phone-numbers-by-id-update.md) | `POST /phone-numbers/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update phone trigger](actions/update-phone-triggers-by-id-update.md) | `POST /phone-triggers/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update shared device](actions/update-share-link-devices-by-id-update.md) | `POST /share-link-devices/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update share link](actions/update-share-links-by-id-update.md) | `POST /share-links/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update shared device](actions/update-shared-devices-by-id-update.md) | `POST /shared-devices/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update share](actions/update-shares-by-id-update.md) | `POST /shares/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update slack webhook](actions/update-slack-webhooks-by-id-update.md) | `POST /slack-webhooks/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update telegram chats's info](actions/update-telegram-chat-ids-by-id-update.md) | `POST /telegram-chat_ids/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update mobile user](actions/update-users-update.md) | `POST /users/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update api token](actions/update-vendor-api-tokens-by-id-update.md) | `POST /vendor/api-tokens/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update build part](actions/update-vendor-build-parts-by-id.md) | `POST /vendor/build-parts/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Update dashboard](actions/update-vendor-dashboards-by-id-update.md) | `POST /vendor/dashboards/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update firmware changelog](actions/update-vendor-firmware-changelogs-by-id-update.md) | `POST /vendor/firmware-changelogs/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update firmware](actions/update-vendor-firmwares-by-id-ap-update.md) | `POST /vendor/firmwares/{id}/ap/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update firmware](actions/update-vendor-firmwares-by-id-update.md) | `POST /vendor/firmwares/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update layout](actions/update-vendor-layouts-by-id-update.md) | `POST /vendor/layouts/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update pairing config](actions/update-vendor-pairing-config-by-id.md) | `POST /vendor/pairing-config/{id}` | [docs](https://cloud.2smart.com/swagger/) |
| [Update product](actions/update-vendor-products-by-id-update.md) | `POST /vendor/products/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Sensor info update](actions/update-vendor-sensors-info-update.md) | `POST /vendor/sensors-info/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update vendor](actions/update-vendor-update.md) | `POST /vendor/update` | [docs](https://cloud.2smart.com/swagger/) |
| [Update WhatsApp chats's info](actions/update-whatsapp-chat-ids-by-id-update.md) | `POST /whatsapp-chat_ids/{id}/update` | [docs](https://cloud.2smart.com/swagger/) |
