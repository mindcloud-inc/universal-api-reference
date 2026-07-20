# Flespi: Native API Reference

A consolidated summary of Flespi's API configuration and 365 documented operations, with links to official documentation.

- **Official docs:** https://flespi.com/rest-api
- **OpenAPI specification:** https://flespi.io/gw/api.json
- **API base URL:** `https://flespi.io`

## Authentication

### Flespi token

Authenticate Flespi REST requests with an Authorization header using the FlespiToken prefix.

### Credentials

- **API key:** `apiKey` · required · Flespi token value only. Do not include the FlespiToken prefix.

[Official authentication documentation](https://flespi.com/rest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (365 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate intervals from AI logs](actions/create-ai-logs-calculate.md) | `POST /ai/logs/calculate` | [docs](https://flespi.io/docs/) |
| [MCP server for development agents](actions/create-ai-mcp-develop.md) | `POST /ai/mcp/develop` | [docs](https://flespi.io/docs/) |
| [MCP server for support agents](actions/create-ai-mcp-support.md) | `POST /ai/mcp/support` | [docs](https://flespi.io/docs/) |
| [Consult flespi account expert](actions/create-ai-tools-consult-flespi-account.md) | `POST /ai/tools/consult-flespi-account` | [docs](https://flespi.io/docs/) |
| [Generate flespi expression](actions/create-ai-tools-generate-flespi-expression.md) | `POST /ai/tools/generate-flespi-expression` | [docs](https://flespi.io/docs/) |
| [Generate PVM code](actions/create-ai-tools-generate-pvm-code.md) | `POST /ai/tools/generate-pvm-code` | [docs](https://flespi.io/docs/) |
| [Retrieve REST API method schema](actions/create-ai-tools-get-api-schema.md) | `POST /ai/tools/get-api-schema` | [docs](https://flespi.io/docs/) |
| [Search for REST API methods](actions/create-ai-tools-search-api-methods.md) | `POST /ai/tools/search-api-methods` | [docs](https://flespi.io/docs/) |
| [Search device documentation](actions/create-ai-tools-search-device-documentation.md) | `POST /ai/tools/search-device-documentation` | [docs](https://flespi.io/docs/) |
| [Search flespi platform documentation](actions/create-ai-tools-search-flespi-documentation.md) | `POST /ai/tools/search-flespi-documentation` | [docs](https://flespi.io/docs/) |
| [Accept/deny flespi account rules](actions/create-auth-account-confirm.md) | `POST /auth/account/confirm` | [docs](https://flespi.io/docs/) |
| [Register new flespi account by email](actions/create-auth-account-register.md) | `POST /auth/account/register` | [docs](https://flespi.io/docs/) |
| [Email verification callback](actions/create-auth-email-confirm.md) | `POST /auth/email/confirm` | [docs](https://flespi.io/docs/) |
| [Email verification fallback](actions/create-auth-email-revert.md) | `POST /auth/email/revert` | [docs](https://flespi.io/docs/) |
| [Login to the flespi panel using email and password](actions/create-auth-login-credentials.md) | `POST /auth/login/credentials` | [docs](https://flespi.io/docs/) |
| [Request passwordless login link](actions/create-auth-login-passwordless.md) | `POST /auth/login/passwordless` | [docs](https://flespi.io/docs/) |
| [Passwordless login confirmation](actions/create-auth-login-passwordless-confirm.md) | `POST /auth/login/passwordless/confirm` | [docs](https://flespi.io/docs/) |
| [Create new asset](actions/create-gw-assets.md) | `POST /gw/assets` | [docs](https://flespi.io/docs/) |
| [Post Gw Assets Intervals](actions/create-gw-assets-assets-selector-intervals.md) | `POST /gw/assets/{assets.selector}/intervals` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from asset logs](actions/create-gw-assets-assets-selector-logs-calculate.md) | `POST /gw/assets/{assets.selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create calculator configuration](actions/create-gw-calcs.md) | `POST /gw/calcs` | [docs](https://flespi.io/docs/) |
| [Assign assets to calc](actions/create-gw-calcs-calcs-selector-assets-calc-assets-selector.md) | `POST /gw/calcs/{calcs.selector}/assets/{calc.assets.selector}` | [docs](https://flespi.io/docs/) |
| [Split calculated intervals on a higher level intervals](actions/create-gw-calcs-calcs-selector-devices-calc-devices-selector-calculate.md) | `POST /gw/calcs/{calcs.selector}/devices/{calc.devices.selector}/calculate` | [docs](https://flespi.io/docs/) |
| [Recalculate assigned device intervals](actions/create-gw-calcs-calcs-selector-devices-calc-devices-selector-recalculate.md) | `POST /gw/calcs/{calcs.selector}/devices/{calc.devices.selector}/recalculate` | [docs](https://flespi.io/docs/) |
| [Assign devices to calculator](actions/create-gw-calcs-calcs-selector-devices-dev-selector.md) | `POST /gw/calcs/{calcs.selector}/devices/{dev-selector}` | [docs](https://flespi.io/docs/) |
| [Assign geofences to calc](actions/create-gw-calcs-calcs-selector-geofences-calc-geofences-selector.md) | `POST /gw/calcs/{calcs.selector}/geofences/{calc.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Assign a group of devices to a calculator](actions/create-gw-calcs-calcs-selector-groups-calc-groups-selector.md) | `POST /gw/calcs/{calcs.selector}/groups/{calc.groups.selector}` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from calculator logs](actions/create-gw-calcs-calcs-selector-logs-calculate.md) | `POST /gw/calcs/{calcs.selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create new channel](actions/create-gw-channels.md) | `POST /gw/channels` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from channel logs](actions/create-gw-channels-ch-selector-logs-calculate.md) | `POST /gw/channels/{ch-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create new device](actions/create-gw-devices.md) | `POST /gw/devices` | [docs](https://flespi.io/docs/) |
| [Split devices messages into intervals (run reports)](actions/create-gw-devices-dev-selector-calculate.md) | `POST /gw/devices/{dev-selector}/calculate` | [docs](https://flespi.io/docs/) |
| [Send command to the connected device in real-time](actions/create-gw-devices-dev-selector-commands.md) | `POST /gw/devices/{dev-selector}/commands` | [docs](https://flespi.io/docs/) |
| [Schedule command execution](actions/create-gw-devices-dev-selector-commands-queue.md) | `POST /gw/devices/{dev-selector}/commands-queue` | [docs](https://flespi.io/docs/) |
| [Assign geofences to device](actions/create-gw-devices-dev-selector-geofences-dev-geofences-selector.md) | `POST /gw/devices/{dev-selector}/geofences/{dev-geofences-selector}` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from device logs](actions/create-gw-devices-dev-selector-logs-calculate.md) | `POST /gw/devices/{dev-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Upload media file to device](actions/create-gw-devices-dev-selector-media.md) | `POST /gw/devices/{dev-selector}/media` | [docs](https://flespi.io/docs/) |
| [Register messages into device](actions/create-gw-devices-dev-selector-messages.md) | `POST /gw/devices/{dev-selector}/messages` | [docs](https://flespi.io/docs/) |
| [Send SMS command to the device in real-time](actions/create-gw-devices-dev-selector-sms.md) | `POST /gw/devices/{dev-selector}/sms` | [docs](https://flespi.io/docs/) |
| [Create new geofence](actions/create-gw-geofences.md) | `POST /gw/geofences` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from geofence logs](actions/create-gw-geofences-geofences-selector-logs-calculate.md) | `POST /gw/geofences/{geofences.selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create new group](actions/create-gw-groups.md) | `POST /gw/groups` | [docs](https://flespi.io/docs/) |
| [Assign assets to group](actions/create-gw-groups-groups-selector-assets-group-assets-selector.md) | `POST /gw/groups/{groups.selector}/assets/{group.assets.selector}` | [docs](https://flespi.io/docs/) |
| [Assign devices to group](actions/create-gw-groups-groups-selector-devices-group-devices-selector.md) | `POST /gw/groups/{groups.selector}/devices/{group.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Assign geofences to group](actions/create-gw-groups-groups-selector-geofences-group-geofences-selector.md) | `POST /gw/groups/{groups.selector}/geofences/{group.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from group logs](actions/create-gw-groups-groups-selector-logs-calculate.md) | `POST /gw/groups/{groups.selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create modem](actions/create-gw-modems.md) | `POST /gw/modems` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from modem logs](actions/create-gw-modems-modem-selector-logs-calculate.md) | `POST /gw/modems/{modem-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create new plugin](actions/create-gw-plugins.md) | `POST /gw/plugins` | [docs](https://flespi.io/docs/) |
| [Assign devices to plugin](actions/create-gw-plugins-plugin-selector-devices-plugin-devices-selector.md) | `POST /gw/plugins/{plugin.selector}/devices/{plugin.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Assign geofences to plugin](actions/create-gw-plugins-plugin-selector-geofences-plugin-geofences-selector.md) | `POST /gw/plugins/{plugin.selector}/geofences/{plugin.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Assign a group of devices to a plugin](actions/create-gw-plugins-plugin-selector-groups-plugin-groups-selector.md) | `POST /gw/plugins/{plugin.selector}/groups/{plugin.groups.selector}` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from plugin logs](actions/create-gw-plugins-plugin-selector-logs-calculate.md) | `POST /gw/plugins/{plugin.selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create new stream](actions/create-gw-streams.md) | `POST /gw/streams` | [docs](https://flespi.io/docs/) |
| [Subscribe stream to channel messages](actions/create-gw-streams-stream-selector-channels-stream-channels-selector.md) | `POST /gw/streams/{stream.selector}/channels/{stream.channels.selector}` | [docs](https://flespi.io/docs/) |
| [Subscribe stream to device messages](actions/create-gw-streams-stream-selector-devices-stream-devices-selector.md) | `POST /gw/streams/{stream.selector}/devices/{stream.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Assign geofences to stream](actions/create-gw-streams-stream-selector-geofences-stream-geofences-selector.md) | `POST /gw/streams/{stream.selector}/geofences/{stream.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Subscribe stream to group of devices](actions/create-gw-streams-stream-selector-groups-stream-groups-selector.md) | `POST /gw/streams/{stream.selector}/groups/{stream.groups.selector}` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from stream logs](actions/create-gw-streams-stream-selector-logs-calculate.md) | `POST /gw/streams/{stream.selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Post messages to stream queue](actions/create-gw-streams-stream-selector-messages.md) | `POST /gw/streams/{stream.selector}/messages` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from MQTT broker logs](actions/create-mqtt-logs-calculate.md) | `POST /mqtt/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Publish MQTT message](actions/create-mqtt-messages.md) | `POST /mqtt/messages` | [docs](https://flespi.io/docs/) |
| [Create persistent MQTT session](actions/create-mqtt-sessions.md) | `POST /mqtt/sessions` | [docs](https://flespi.io/docs/) |
| [Subscribe MQTT session to a topic](actions/create-mqtt-sessions-sessions-selector-subscriptions.md) | `POST /mqtt/sessions/{sessions-selector}/subscriptions` | [docs](https://flespi.io/docs/) |
| [Attempt to charge invoice](actions/create-platform-billing-invoices-invoices-selector-charge.md) | `POST /platform/billing/invoices/{invoices-selector}/charge` | [docs](https://flespi.io/docs/) |
| [Post message adressed to flespi support.](actions/create-platform-customer-chat.md) | `POST /platform/customer/chat` | [docs](https://flespi.io/docs/) |
| [Control AI assistant](actions/create-platform-customer-chat-ai-assistant.md) | `POST /platform/customer/chat/ai-assistant` | [docs](https://flespi.io/docs/) |
| [Attach file to flespi support chat.](actions/create-platform-customer-chat-file.md) | `POST /platform/customer/chat-file` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from customer logs](actions/create-platform-customer-logs-calculate.md) | `POST /platform/customer/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from deleted item logs](actions/create-platform-deleted-deleted-selector-logs-calculate.md) | `POST /platform/deleted/{deleted-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Try to restore deleted items.](actions/create-platform-deleted-deleted-selector-restore.md) | `POST /platform/deleted/{deleted-selector}/restore` | [docs](https://flespi.io/docs/) |
| [Create grant](actions/create-platform-grants.md) | `POST /platform/grants` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from grant logs](actions/create-platform-grants-grants-selector-logs-calculate.md) | `POST /platform/grants/{grants-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Grant items access to subaccount](actions/create-platform-grants-grants-selector-subaccounts-grant-subaccounts-selector.md) | `POST /platform/grants/{grants-selector}/subaccounts/{grant-subaccounts-selector}` | [docs](https://flespi.io/docs/) |
| [Create Identity Provider](actions/create-platform-identity-providers.md) | `POST /platform/identity-providers` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from identity provider logs](actions/create-platform-identity-providers-identity-provider-selector-logs-calculate.md) | `POST /platform/identity-providers/{identity-provider-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create subaccount limit](actions/create-platform-limits.md) | `POST /platform/limits` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from limit logs](actions/create-platform-limits-limits-selector-logs-calculate.md) | `POST /platform/limits/{limits-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create realm](actions/create-platform-realms.md) | `POST /platform/realms` | [docs](https://flespi.io/docs/) |
| [Bind Identity Provider to the realm](actions/create-platform-realms-realm-selector-identity-providers-realm-identity-provider-selector.md) | `POST /platform/realms/{realm-selector}/identity-providers/{realm-identity-provider-selector}` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from realm logs](actions/create-platform-realms-realm-selector-logs-calculate.md) | `POST /platform/realms/{realm-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create new role](actions/create-platform-realms-realm-selector-roles.md) | `POST /platform/realms/{realm-selector}/roles` | [docs](https://flespi.io/docs/) |
| [Create new realm user](actions/create-platform-realms-realm-selector-users.md) | `POST /platform/realms/{realm-selector}/users` | [docs](https://flespi.io/docs/) |
| [Log in as user](actions/create-platform-realms-realm-selector-users-user-selector-login.md) | `POST /platform/realms/{realm-selector}/users/{user-selector}/login` | [docs](https://flespi.io/docs/) |
| [Log out user](actions/create-platform-realms-realm-selector-users-user-selector-logout.md) | `POST /platform/realms/{realm-selector}/users/{user-selector}/logout` | [docs](https://flespi.io/docs/) |
| [Create subaccount](actions/create-platform-subaccounts.md) | `POST /platform/subaccounts` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from subaccount logs](actions/create-platform-subaccounts-subaccounts-selector-logs-calculate.md) | `POST /platform/subaccounts/{subaccounts-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create token](actions/create-platform-tokens.md) | `POST /platform/tokens` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from token logs](actions/create-platform-tokens-tokens-selector-logs-calculate.md) | `POST /platform/tokens/{tokens-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create webhook](actions/create-platform-webhooks.md) | `POST /platform/webhooks` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from webhook logs](actions/create-platform-webhooks-webhooks-selector-logs-calculate.md) | `POST /platform/webhooks/{webhooks-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Confirm realm user registration](actions/create-realm-realm-public-id-confirm.md) | `POST /realm/{realm-public-id}/confirm` | [docs](https://flespi.io/docs/) |
| [Authorize realm user](actions/create-realm-realm-public-id-login.md) | `POST /realm/{realm-public-id}/login` | [docs](https://flespi.io/docs/) |
| [Create new CDN](actions/create-storage-cdns.md) | `POST /storage/cdns` | [docs](https://flespi.io/docs/) |
| [Upload files to CDN](actions/create-storage-cdns-cdn-selector-files.md) | `POST /storage/cdns/{cdn-selector}/files` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from CDN logs](actions/create-storage-cdns-cdn-selector-logs-calculate.md) | `POST /storage/cdns/{cdn-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Create new container](actions/create-storage-containers.md) | `POST /storage/containers` | [docs](https://flespi.io/docs/) |
| [Split container messages into intervals](actions/create-storage-containers-container-selector-calculate.md) | `POST /storage/containers/{container-selector}/calculate` | [docs](https://flespi.io/docs/) |
| [Calculate intervals from container logs](actions/create-storage-containers-container-selector-logs-calculate.md) | `POST /storage/containers/{container-selector}/logs/calculate` | [docs](https://flespi.io/docs/) |
| [Post messages to container](actions/create-storage-containers-container-selector-messages.md) | `POST /storage/containers/{container-selector}/messages` | [docs](https://flespi.io/docs/) |
| [Test expression evaluation](actions/create-storage-expressions-test.md) | `POST /storage/expressions/test` | [docs](https://flespi.io/docs/) |
| [Delete selected assets](actions/delete-gw-assets-assets-selector.md) | `DELETE /gw/assets/{assets.selector}` | [docs](https://flespi.io/docs/) |
| [Delete calculator and all calculated intervals from assigned devices](actions/delete-gw-calcs-calcs-selector.md) | `DELETE /gw/calcs/{calcs.selector}` | [docs](https://flespi.io/docs/) |
| [Unassign assets from calc](actions/delete-gw-calcs-calcs-selector-assets-calc-assets-selector.md) | `DELETE /gw/calcs/{calcs.selector}/assets/{calc.assets.selector}` | [docs](https://flespi.io/docs/) |
| [Unassign device from calculator](actions/delete-gw-calcs-calcs-selector-devices-calc-devices-selector.md) | `DELETE /gw/calcs/{calcs.selector}/devices/{calc.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Unassign geofences from calc](actions/delete-gw-calcs-calcs-selector-geofences-calc-geofences-selector.md) | `DELETE /gw/calcs/{calcs.selector}/geofences/{calc.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Unassign a group from calculator](actions/delete-gw-calcs-calcs-selector-groups-calc-groups-selector.md) | `DELETE /gw/calcs/{calcs.selector}/groups/{calc.groups.selector}` | [docs](https://flespi.io/docs/) |
| [Delete channels](actions/delete-gw-channels-ch-selector.md) | `DELETE /gw/channels/{ch-selector}` | [docs](https://flespi.io/docs/) |
| [Close TCP connections](actions/delete-gw-channels-ch-selector-connections-conn-selector.md) | `DELETE /gw/channels/{ch-selector}/connections/{conn-selector}` | [docs](https://flespi.io/docs/) |
| [Delete messages from channel buffer](actions/delete-gw-channels-ch-selector-messages.md) | `DELETE /gw/channels/{ch-selector}/messages` | [docs](https://flespi.io/docs/) |
| [Delete selected devices](actions/delete-gw-devices-dev-selector.md) | `DELETE /gw/devices/{dev-selector}` | [docs](https://flespi.io/docs/) |
| [Remove command from queue](actions/delete-gw-devices-dev-selector-commands-queue-devices-commands-queue-selector.md) | `DELETE /gw/devices/{dev-selector}/commands-queue/{devices.commands-queue.selector}` | [docs](https://flespi.io/docs/) |
| [Close TCP connections](actions/delete-gw-devices-dev-selector-connections-conn-selector.md) | `DELETE /gw/devices/{dev-selector}/connections/{conn-selector}` | [docs](https://flespi.io/docs/) |
| [Unassign geofences from device](actions/delete-gw-devices-dev-selector-geofences-dev-geofences-selector.md) | `DELETE /gw/devices/{dev-selector}/geofences/{dev-geofences-selector}` | [docs](https://flespi.io/docs/) |
| [Delete media files](actions/delete-gw-devices-dev-selector-media.md) | `DELETE /gw/devices/{dev-selector}/media` | [docs](https://flespi.io/docs/) |
| [Re-read setting value from the device or cancel setting update request](actions/delete-gw-devices-dev-selector-settings-sett-selector.md) | `DELETE /gw/devices/{dev-selector}/settings/{sett-selector}` | [docs](https://flespi.io/docs/) |
| [Delete device telemetry fields](actions/delete-gw-devices-dev-selector-telemetry-telemetry-selector.md) | `DELETE /gw/devices/{dev-selector}/telemetry/{telemetry-selector}` | [docs](https://flespi.io/docs/) |
| [Delete selected geofences](actions/delete-gw-geofences-geofences-selector.md) | `DELETE /gw/geofences/{geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Delete selected groups](actions/delete-gw-groups-groups-selector.md) | `DELETE /gw/groups/{groups.selector}` | [docs](https://flespi.io/docs/) |
| [Unassign assets from group](actions/delete-gw-groups-groups-selector-assets-group-assets-selector.md) | `DELETE /gw/groups/{groups.selector}/assets/{group.assets.selector}` | [docs](https://flespi.io/docs/) |
| [Unassign devices from group](actions/delete-gw-groups-groups-selector-devices-group-devices-selector.md) | `DELETE /gw/groups/{groups.selector}/devices/{group.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Unassign geofences from group](actions/delete-gw-groups-groups-selector-geofences-group-geofences-selector.md) | `DELETE /gw/groups/{groups.selector}/geofences/{group.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Delete modem](actions/delete-gw-modems-modem-selector.md) | `DELETE /gw/modems/{modem-selector}` | [docs](https://flespi.io/docs/) |
| [Delete selected plugins](actions/delete-gw-plugins-plugin-selector.md) | `DELETE /gw/plugins/{plugin.selector}` | [docs](https://flespi.io/docs/) |
| [Unassign device from group](actions/delete-gw-plugins-plugin-selector-devices-plugin-devices-selector.md) | `DELETE /gw/plugins/{plugin.selector}/devices/{plugin.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Unassign geofences from plugin](actions/delete-gw-plugins-plugin-selector-geofences-plugin-geofences-selector.md) | `DELETE /gw/plugins/{plugin.selector}/geofences/{plugin.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Unassign a group from plugin](actions/delete-gw-plugins-plugin-selector-groups-plugin-groups-selector.md) | `DELETE /gw/plugins/{plugin.selector}/groups/{plugin.groups.selector}` | [docs](https://flespi.io/docs/) |
| [Delete selected streams](actions/delete-gw-streams-stream-selector.md) | `DELETE /gw/streams/{stream.selector}` | [docs](https://flespi.io/docs/) |
| [Unsubscribe stream from channels](actions/delete-gw-streams-stream-selector-channels-stream-channels-selector.md) | `DELETE /gw/streams/{stream.selector}/channels/{stream.channels.selector}` | [docs](https://flespi.io/docs/) |
| [Unsubscribe stream from devices](actions/delete-gw-streams-stream-selector-devices-stream-devices-selector.md) | `DELETE /gw/streams/{stream.selector}/devices/{stream.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Unassign geofences from stream](actions/delete-gw-streams-stream-selector-geofences-stream-geofences-selector.md) | `DELETE /gw/streams/{stream.selector}/geofences/{stream.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Unsubscribe stream from group](actions/delete-gw-streams-stream-selector-groups-stream-groups-selector.md) | `DELETE /gw/streams/{stream.selector}/groups/{stream.groups.selector}` | [docs](https://flespi.io/docs/) |
| [Remove all messages from the stream queue.](actions/delete-gw-streams-stream-selector-messages.md) | `DELETE /gw/streams/{stream.selector}/messages` | [docs](https://flespi.io/docs/) |
| [Delete retained MQTT messages](actions/delete-mqtt-messages-messages-selector.md) | `DELETE /mqtt/messages/{messages-selector}` | [docs](https://flespi.io/docs/) |
| [Delete MQTT session](actions/delete-mqtt-sessions-sessions-selector.md) | `DELETE /mqtt/sessions/{sessions-selector}` | [docs](https://flespi.io/docs/) |
| [Unsubscribe MQTT session from topic](actions/delete-mqtt-sessions-sessions-selector-subscriptions-subscriptions-selector.md) | `DELETE /mqtt/sessions/{sessions-selector}/subscriptions/{subscriptions-selector}` | [docs](https://flespi.io/docs/) |
| [Delete the grantors](actions/delete-platform-grantors-grants-selector.md) | `DELETE /platform/grantors/{grants-selector}` | [docs](https://flespi.io/docs/) |
| [Delete grant](actions/delete-platform-grants-grants-selector.md) | `DELETE /platform/grants/{grants-selector}` | [docs](https://flespi.io/docs/) |
| [Revoke items access for subaccount](actions/delete-platform-grants-grants-selector-subaccounts-grant-subaccounts-selector.md) | `DELETE /platform/grants/{grants-selector}/subaccounts/{grant-subaccounts-selector}` | [docs](https://flespi.io/docs/) |
| [Delete Identity Providers](actions/delete-platform-identity-providers-identity-provider-selector.md) | `DELETE /platform/identity-providers/{identity-provider-selector}` | [docs](https://flespi.io/docs/) |
| [Delete subaccount limits](actions/delete-platform-limits-limits-selector.md) | `DELETE /platform/limits/{limits-selector}` | [docs](https://flespi.io/docs/) |
| [Detach selected OAuth profiles from flespi customer](actions/delete-platform-oauth-oauth-selector.md) | `DELETE /platform/oauth/{oauth-selector}` | [docs](https://flespi.io/docs/) |
| [Delete realm](actions/delete-platform-realms-realm-selector.md) | `DELETE /platform/realms/{realm-selector}` | [docs](https://flespi.io/docs/) |
| [Remove binding of Identity Provider from realms](actions/delete-platform-realms-realm-selector-identity-providers-realm-identity-provider-selector.md) | `DELETE /platform/realms/{realm-selector}/identity-providers/{realm-identity-provider-selector}` | [docs](https://flespi.io/docs/) |
| [Delete realm roles](actions/delete-platform-realms-realm-selector-roles-role-selector.md) | `DELETE /platform/realms/{realm-selector}/roles/{role-selector}` | [docs](https://flespi.io/docs/) |
| [Delete realm users](actions/delete-platform-realms-realm-selector-users-user-selector.md) | `DELETE /platform/realms/{realm-selector}/users/{user-selector}` | [docs](https://flespi.io/docs/) |
| [Unlink identity provider accounts from user](actions/delete-platform-realms-realm-selector-users-user-selector-identity-providers-user-identity-provider-selector.md) | `DELETE /platform/realms/{realm-selector}/users/{user-selector}/identity-providers/{user-identity-provider-selector}` | [docs](https://flespi.io/docs/) |
| [Reset user's password](actions/delete-platform-realms-realm-selector-users-user-selector-password.md) | `DELETE /platform/realms/{realm-selector}/users/{user-selector}/password` | [docs](https://flespi.io/docs/) |
| [Delete subaccount](actions/delete-platform-subaccounts-subaccounts-selector.md) | `DELETE /platform/subaccounts/{subaccounts-selector}` | [docs](https://flespi.io/docs/) |
| [Delete token](actions/delete-platform-tokens-tokens-selector.md) | `DELETE /platform/tokens/{tokens-selector}` | [docs](https://flespi.io/docs/) |
| [Delete webhook](actions/delete-platform-webhooks-webhooks-selector.md) | `DELETE /platform/webhooks/{webhooks-selector}` | [docs](https://flespi.io/docs/) |
| [Delete selected CDNs](actions/delete-storage-cdns-cdn-selector.md) | `DELETE /storage/cdns/{cdn-selector}` | [docs](https://flespi.io/docs/) |
| [Delete files from CDN](actions/delete-storage-cdns-cdn-selector-files.md) | `DELETE /storage/cdns/{cdn-selector}/files` | [docs](https://flespi.io/docs/) |
| [Delete selected containers](actions/delete-storage-containers-container-selector.md) | `DELETE /storage/containers/{container-selector}` | [docs](https://flespi.io/docs/) |
| [Delete messages from container](actions/delete-storage-containers-container-selector-messages.md) | `DELETE /storage/containers/{container-selector}/messages` | [docs](https://flespi.io/docs/) |
| [Get AI development MCP schema](actions/get-ai-development-mcp-schema.md) | `GET /ai/mcp/develop` | [docs](https://flespi.io/docs/#/ai/mcp/get_mcp_develop) |
| [Get AI logs](actions/get-ai-logs.md) | `GET /ai/logs` | [docs](https://flespi.io/docs/#/ai/logs/get_logs) |
| [Get AI support MCP schema](actions/get-ai-support-mcp-schema.md) | `GET /ai/mcp/support` | [docs](https://flespi.io/docs/#/ai/mcp/get_mcp_support) |
| [Identity provider callback](actions/get-auth-callback.md) | `GET /auth/callback` | [docs](https://flespi.io/docs/) |
| [Identity provider proxy callback](actions/get-auth-callback-proxy.md) | `GET /auth/callback/proxy` | [docs](https://flespi.io/docs/) |
| [Retrieve token information](actions/get-auth-info.md) | `GET /auth/info` | [docs](https://flespi.io/docs/) |
| [Link OAuth account to the flespi account](actions/get-auth-oauth-link.md) | `GET /auth/oauth/link` | [docs](https://flespi.io/docs/) |
| [Login and register to flespi](actions/get-auth-oauth-login.md) | `GET /auth/oauth/login` | [docs](https://flespi.io/docs/) |
| [List supported OAuth providers](actions/get-auth-oauth-providers.md) | `GET /auth/oauth/providers` | [docs](https://flespi.io/docs/) |
| [Fetch available flespi regions](actions/get-auth-regions.md) | `GET /auth/regions` | [docs](https://flespi.io/docs/) |
| [Get devices by selector](actions/get-devices-by-selector.md) | `GET /gw/devices/{dev-selector}` | [docs](https://flespi.io/docs/#/gw/devices/get_devices_dev_selector) |
| [List available assets](actions/get-gw-assets-assets-selector.md) | `GET /gw/assets/{assets.selector}` | [docs](https://flespi.io/docs/) |
| [Get Gw Assets Intervals](actions/get-gw-assets-assets-selector-intervals.md) | `GET /gw/assets/{assets.selector}/intervals` | [docs](https://flespi.io/docs/) |
| [Retrieve asset logs](actions/get-gw-assets-assets-selector-logs.md) | `GET /gw/assets/{assets.selector}/logs` | [docs](https://flespi.io/docs/) |
| [Retrieve calculator configuration](actions/get-gw-calcs-calcs-selector.md) | `GET /gw/calcs/{calcs.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve assets in calc](actions/get-gw-calcs-calcs-selector-assets-calc-assets-selector.md) | `GET /gw/calcs/{calcs.selector}/assets/{calc.assets.selector}` | [docs](https://flespi.io/docs/) |
| [List devices assigned to calculator](actions/get-gw-calcs-calcs-selector-devices-calc-devices-selector.md) | `GET /gw/calcs/{calcs.selector}/devices/{calc.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve calculated device intervals](actions/get-gw-calcs-calcs-selector-devices-calc-devices-selector-intervals-calc-device-intervals-selector.md) | `GET /gw/calcs/{calcs.selector}/devices/{calc.devices.selector}/intervals/{calc.device.intervals.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve geofences in calc](actions/get-gw-calcs-calcs-selector-geofences-calc-geofences-selector.md) | `GET /gw/calcs/{calcs.selector}/geofences/{calc.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Fetch groups assigned to the calculator](actions/get-gw-calcs-calcs-selector-groups-calc-groups-selector.md) | `GET /gw/calcs/{calcs.selector}/groups/{calc.groups.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve calculator logs](actions/get-gw-calcs-calcs-selector-logs.md) | `GET /gw/calcs/{calcs.selector}/logs` | [docs](https://flespi.io/docs/) |
| [Fetch available channel protocols](actions/get-gw-channel-protocols-channel-protocols-selector.md) | `GET /gw/channel-protocols/{channel-protocols.selector}` | [docs](https://flespi.io/docs/) |
| [Get available device types withing selected channel protocols](actions/get-gw-channel-protocols-channel-protocols-selector-device-types-devtypes-selector.md) | `GET /gw/channel-protocols/{channel-protocols.selector}/device-types/{devtypes.selector}` | [docs](https://flespi.io/docs/) |
| [List available channels](actions/get-gw-channels-ch-selector.md) | `GET /gw/channels/{ch-selector}` | [docs](https://flespi.io/docs/) |
| [List active channel TCP connections](actions/get-gw-channels-ch-selector-connections-conn-selector.md) | `GET /gw/channels/{ch-selector}/connections/{conn-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve raw traffic for ident](actions/get-gw-channels-ch-selector-idents-ch-ident-selector-packets.md) | `GET /gw/channels/{ch-selector}/idents/{ch-ident-selector}/packets` | [docs](https://flespi.io/docs/) |
| [List idents reported to the channel](actions/get-gw-channels-ch-selector-idents-channel-ident-selector.md) | `GET /gw/channels/{ch-selector}/idents/{channel.ident.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve channel logs](actions/get-gw-channels-ch-selector-logs.md) | `GET /gw/channels/{ch-selector}/logs` | [docs](https://flespi.io/docs/) |
| [Read messages from channel buffer](actions/get-gw-channels-ch-selector-messages.md) | `GET /gw/channels/{ch-selector}/messages` | [docs](https://flespi.io/docs/) |
| [Retrieve list of queued commands](actions/get-gw-devices-dev-selector-commands-queue-devices-commands-queue-selector.md) | `GET /gw/devices/{dev-selector}/commands-queue/{devices.commands-queue.selector}` | [docs](https://flespi.io/docs/) |
| [Get executed or expired commands](actions/get-gw-devices-dev-selector-commands-result.md) | `GET /gw/devices/{dev-selector}/commands-result` | [docs](https://flespi.io/docs/) |
| [Get executed or expired command by its ID](actions/get-gw-devices-dev-selector-commands-result-command-id-selector.md) | `GET /gw/devices/{dev-selector}/commands-result/{command-id-selector}` | [docs](https://flespi.io/docs/) |
| [List active TCP connections](actions/get-gw-devices-dev-selector-connections-conn-selector.md) | `GET /gw/devices/{dev-selector}/connections/{conn-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve geofences in device](actions/get-gw-devices-dev-selector-geofences-dev-geofences-selector.md) | `GET /gw/devices/{dev-selector}/geofences/{dev-geofences-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve device logs](actions/get-gw-devices-dev-selector-logs.md) | `GET /gw/devices/{dev-selector}/logs` | [docs](https://flespi.io/docs/) |
| [List device media files](actions/get-gw-devices-dev-selector-media.md) | `GET /gw/devices/{dev-selector}/media` | [docs](https://flespi.io/docs/) |
| [Retrieve messages stored by the device](actions/get-gw-devices-dev-selector-messages.md) | `GET /gw/devices/{dev-selector}/messages` | [docs](https://flespi.io/docs/) |
| [Retrieve raw device traffic](actions/get-gw-devices-dev-selector-packets.md) | `GET /gw/devices/{dev-selector}/packets` | [docs](https://flespi.io/docs/) |
| [Retrieve device settings](actions/get-gw-devices-dev-selector-settings-sett-selector.md) | `GET /gw/devices/{dev-selector}/settings/{sett-selector}` | [docs](https://flespi.io/docs/) |
| [Generate SMS message text for the command](actions/get-gw-devices-dev-selector-sms.md) | `GET /gw/devices/{dev-selector}/sms` | [docs](https://flespi.io/docs/) |
| [Retrieve device telemetry](actions/get-gw-devices-dev-selector-telemetry-telemetry-selector.md) | `GET /gw/devices/{dev-selector}/telemetry/{telemetry-selector}` | [docs](https://flespi.io/docs/) |
| [List available geofences](actions/get-gw-geofences-geofences-selector.md) | `GET /gw/geofences/{geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Test if the point is inside geofences.](actions/get-gw-geofences-geofences-selector-hittest.md) | `GET /gw/geofences/{geofences.selector}/hittest` | [docs](https://flespi.io/docs/) |
| [Retrieve geofence logs](actions/get-gw-geofences-geofences-selector-logs.md) | `GET /gw/geofences/{geofences.selector}/logs` | [docs](https://flespi.io/docs/) |
| [List available groups](actions/get-gw-groups-groups-selector.md) | `GET /gw/groups/{groups.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve assets in group](actions/get-gw-groups-groups-selector-assets-group-assets-selector.md) | `GET /gw/groups/{groups.selector}/assets/{group.assets.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve devices in group](actions/get-gw-groups-groups-selector-devices-group-devices-selector.md) | `GET /gw/groups/{groups.selector}/devices/{group.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve geofences in group](actions/get-gw-groups-groups-selector-geofences-group-geofences-selector.md) | `GET /gw/groups/{groups.selector}/geofences/{group.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve group logs](actions/get-gw-groups-groups-selector-logs.md) | `GET /gw/groups/{groups.selector}/logs` | [docs](https://flespi.io/docs/) |
| [Fetch standard message parameters](actions/get-gw-message-parameters-message-parameter-selector.md) | `GET /gw/message-parameters/{message-parameter.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve modems](actions/get-gw-modems-modem-selector.md) | `GET /gw/modems/{modem-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve modem logs](actions/get-gw-modems-modem-selector-logs.md) | `GET /gw/modems/{modem-selector}/logs` | [docs](https://flespi.io/docs/) |
| [Fetch available plugin types](actions/get-gw-plugin-types-plugin-types-selector.md) | `GET /gw/plugin-types/{plugin-types.selector}` | [docs](https://flespi.io/docs/) |
| [List available plugins](actions/get-gw-plugins-plugin-selector.md) | `GET /gw/plugins/{plugin.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve devices in plugin](actions/get-gw-plugins-plugin-selector-devices-plugin-devices-selector.md) | `GET /gw/plugins/{plugin.selector}/devices/{plugin.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve geofences in plugin](actions/get-gw-plugins-plugin-selector-geofences-plugin-geofences-selector.md) | `GET /gw/plugins/{plugin.selector}/geofences/{plugin.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Fetch groups assigned to the plugin](actions/get-gw-plugins-plugin-selector-groups-plugin-groups-selector.md) | `GET /gw/plugins/{plugin.selector}/groups/{plugin.groups.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve plugin logs](actions/get-gw-plugins-plugin-selector-logs.md) | `GET /gw/plugins/{plugin.selector}/logs` | [docs](https://flespi.io/docs/) |
| [Retrieve raw traffic generated by plugin](actions/get-gw-plugins-plugin-selector-packets.md) | `GET /gw/plugins/{plugin.selector}/packets` | [docs](https://flespi.io/docs/) |
| [Fetch available stream protocols](actions/get-gw-stream-protocols-stream-protocols-selector.md) | `GET /gw/stream-protocols/{stream-protocols.selector}` | [docs](https://flespi.io/docs/) |
| [List available streams](actions/get-gw-streams-stream-selector.md) | `GET /gw/streams/{stream.selector}` | [docs](https://flespi.io/docs/) |
| [List channels to which stream is subscribed](actions/get-gw-streams-stream-selector-channels-stream-channels-selector.md) | `GET /gw/streams/{stream.selector}/channels/{stream.channels.selector}` | [docs](https://flespi.io/docs/) |
| [List devices to which stream is subscribed](actions/get-gw-streams-stream-selector-devices-stream-devices-selector.md) | `GET /gw/streams/{stream.selector}/devices/{stream.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve geofences in stream](actions/get-gw-streams-stream-selector-geofences-stream-geofences-selector.md) | `GET /gw/streams/{stream.selector}/geofences/{stream.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [List groups to which stream is subscribed](actions/get-gw-streams-stream-selector-groups-stream-groups-selector.md) | `GET /gw/streams/{stream.selector}/groups/{stream.groups.selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve stream logs](actions/get-gw-streams-stream-selector-logs.md) | `GET /gw/streams/{stream.selector}/logs` | [docs](https://flespi.io/docs/) |
| [Retrieve raw traffic generated by stream](actions/get-gw-streams-stream-selector-packets.md) | `GET /gw/streams/{stream.selector}/packets` | [docs](https://flespi.io/docs/) |
| [Get MQTT logs](actions/get-mqtt-logs.md) | `GET /mqtt/logs` | [docs](https://flespi.io/docs/#/mqtt/logs/get_logs) |
| [Get retained messages](actions/get-mqtt-messages-messages-selector.md) | `GET /mqtt/messages/{messages-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve MQTT sessions](actions/get-mqtt-sessions-sessions-selector.md) | `GET /mqtt/sessions/{sessions-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve MQTT session subscriptions](actions/get-mqtt-sessions-sessions-selector-subscriptions-subscriptions-selector.md) | `GET /mqtt/sessions/{sessions-selector}/subscriptions/{subscriptions-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve customer billing information](actions/get-platform-billing.md) | `GET /platform/billing` | [docs](https://flespi.io/docs/) |
| [Retrieve issued invoices](actions/get-platform-billing-invoices-invoices-selector.md) | `GET /platform/billing/invoices/{invoices-selector}` | [docs](https://flespi.io/docs/) |
| [Fetch payment portal link.](actions/get-platform-billing-payment-portal.md) | `GET /platform/billing/payment_portal` | [docs](https://flespi.io/docs/) |
| [Retrieve customer account information](actions/get-platform-customer.md) | `GET /platform/customer` | [docs](https://flespi.io/docs/) |
| [Retrieve chat communication history between flespi support and customer.](actions/get-platform-customer-chat.md) | `GET /platform/customer/chat` | [docs](https://flespi.io/docs/) |
| [Retrieve knowledge links](actions/get-platform-customer-chat-knowledge.md) | `GET /platform/customer/chat/knowledge` | [docs](https://flespi.io/docs/) |
| [Get platform log records.](actions/get-platform-customer-logs.md) | `GET /platform/customer/logs` | [docs](https://flespi.io/docs/) |
| [Get platform statistics records.](actions/get-platform-customer-statistics.md) | `GET /platform/customer/statistics` | [docs](https://flespi.io/docs/) |
| [Newslist unsubscription callback](actions/get-platform-customer-unsubscribe.md) | `GET /platform/customer/unsubscribe` | [docs](https://flespi.io/docs/) |
| [Get deleted items list. Deleted items are available for logs analyzer up to one month.](actions/get-platform-deleted-deleted-selector.md) | `GET /platform/deleted/{deleted-selector}` | [docs](https://flespi.io/docs/) |
| [Get deleted item logs records.](actions/get-platform-deleted-deleted-selector-logs.md) | `GET /platform/deleted/{deleted-selector}/logs` | [docs](https://flespi.io/docs/) |
| [Retrieve grantors](actions/get-platform-grantors-grants-selector.md) | `GET /platform/grantors/{grants-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve grants](actions/get-platform-grants-grants-selector.md) | `GET /platform/grants/{grants-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve grant logs](actions/get-platform-grants-grants-selector-logs.md) | `GET /platform/grants/{grants-selector}/logs` | [docs](https://flespi.io/docs/) |
| [Get subaccounts to which items access is granted](actions/get-platform-grants-grants-selector-subaccounts-grant-subaccounts-selector.md) | `GET /platform/grants/{grants-selector}/subaccounts/{grant-subaccounts-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve Identity Provider](actions/get-platform-identity-providers-identity-provider-selector.md) | `GET /platform/identity-providers/{identity-provider-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve identity provider logs](actions/get-platform-identity-providers-identity-provider-selector-logs.md) | `GET /platform/identity-providers/{identity-provider-selector}/logs` | [docs](https://flespi.io/docs/) |
| [Retrieve subaccount limits](actions/get-platform-limits-limits-selector.md) | `GET /platform/limits/{limits-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve subaccount limit logs](actions/get-platform-limits-limits-selector-logs.md) | `GET /platform/limits/{limits-selector}/logs` | [docs](https://flespi.io/docs/) |
| [Get customer's OAuth profiles](actions/get-platform-oauth-oauth-selector.md) | `GET /platform/oauth/{oauth-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve realm](actions/get-platform-realms-realm-selector.md) | `GET /platform/realms/{realm-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve Identity Providers binded to realms](actions/get-platform-realms-realm-selector-identity-providers-realm-identity-provider-selector.md) | `GET /platform/realms/{realm-selector}/identity-providers/{realm-identity-provider-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve realm logs](actions/get-platform-realms-realm-selector-logs.md) | `GET /platform/realms/{realm-selector}/logs` | [docs](https://flespi.io/docs/) |
| [Retrieve realm roles](actions/get-platform-realms-realm-selector-roles-role-selector.md) | `GET /platform/realms/{realm-selector}/roles/{role-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve realm users](actions/get-platform-realms-realm-selector-users-user-selector.md) | `GET /platform/realms/{realm-selector}/users/{user-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve user confirmation code](actions/get-platform-realms-realm-selector-users-user-selector-confirmation-password.md) | `GET /platform/realms/{realm-selector}/users/{user-selector}/confirmation/password` | [docs](https://flespi.io/docs/) |
| [Get linked identity provider accounts to user](actions/get-platform-realms-realm-selector-users-user-selector-identity-providers-user-identity-provider-selector.md) | `GET /platform/realms/{realm-selector}/users/{user-selector}/identity-providers/{user-identity-provider-selector}` | [docs](https://flespi.io/docs/) |
| [Get confirmation link for third-party Identity Provider account binding](actions/get-platform-realms-realm-selector-users-user-selector-identity-providers-user-identity-provider-selector-confirmation.md) | `GET /platform/realms/{realm-selector}/users/{user-selector}/identity-providers/{user-identity-provider-selector}/confirmation` | [docs](https://flespi.io/docs/) |
| [Retrieve subaccounts](actions/get-platform-subaccounts-subaccounts-selector.md) | `GET /platform/subaccounts/{subaccounts-selector}` | [docs](https://flespi.io/docs/) |
| [Get subaccount log records.](actions/get-platform-subaccounts-subaccounts-selector-logs.md) | `GET /platform/subaccounts/{subaccounts-selector}/logs` | [docs](https://flespi.io/docs/) |
| [Retrieve tokens](actions/get-platform-tokens-tokens-selector.md) | `GET /platform/tokens/{tokens-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve token logs](actions/get-platform-tokens-tokens-selector-logs.md) | `GET /platform/tokens/{tokens-selector}/logs` | [docs](https://flespi.io/docs/) |
| [Retrieve webhooks](actions/get-platform-webhooks-webhooks-selector.md) | `GET /platform/webhooks/{webhooks-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve webhook logs](actions/get-platform-webhooks-webhooks-selector-logs.md) | `GET /platform/webhooks/{webhooks-selector}/logs` | [docs](https://flespi.io/docs/) |
| [Retrieve raw traffic of actions performed by webhook](actions/get-platform-webhooks-webhooks-selector-packets.md) | `GET /platform/webhooks/{webhooks-selector}/packets` | [docs](https://flespi.io/docs/) |
| [Retrieve identity providers linked with realm](actions/get-realm-realm-public-id-identity-providers.md) | `GET /realm/{realm-public-id}/identity-providers` | [docs](https://flespi.io/docs/) |
| [Retrieve identity provider log in link](actions/get-realm-realm-public-id-identity-providers-identity-provider-id-login.md) | `GET /realm/{realm-public-id}/identity-providers/{identity-provider-id}/login` | [docs](https://flespi.io/docs/) |
| [Retrieve realm information](actions/get-realm-realm-public-id-info.md) | `GET /realm/{realm-public-id}/info` | [docs](https://flespi.io/docs/) |
| [Retrieve realm user information](actions/get-realm-realm-public-id-user.md) | `GET /realm/{realm-public-id}/user` | [docs](https://flespi.io/docs/) |
| [List available CDNs](actions/get-storage-cdns-cdn-selector.md) | `GET /storage/cdns/{cdn-selector}` | [docs](https://flespi.io/docs/) |
| [List CDN files](actions/get-storage-cdns-cdn-selector-files.md) | `GET /storage/cdns/{cdn-selector}/files` | [docs](https://flespi.io/docs/) |
| [Retrieve CDN logs](actions/get-storage-cdns-cdn-selector-logs.md) | `GET /storage/cdns/{cdn-selector}/logs` | [docs](https://flespi.io/docs/) |
| [List available containers](actions/get-storage-containers-container-selector.md) | `GET /storage/containers/{container-selector}` | [docs](https://flespi.io/docs/) |
| [Retrieve container logs](actions/get-storage-containers-container-selector-logs.md) | `GET /storage/containers/{container-selector}/logs` | [docs](https://flespi.io/docs/) |
| [Retrieve messages from container](actions/get-storage-containers-container-selector-messages.md) | `GET /storage/containers/{container-selector}/messages` | [docs](https://flespi.io/docs/) |
| [List asset logs](actions/list-asset-logs.md) | `GET /gw/assets/all/logs` | [docs](https://flespi.io/docs/#/gw/assets/get_assets_assets_selector_logs) |
| [List assets](actions/list-assets.md) | `GET /gw/assets/all` | [docs](https://flespi.io/docs/#/gw/assets/get_assets_assets_selector) |
| [List calculator logs](actions/list-calculator-logs.md) | `GET /gw/calcs/all/logs` | [docs](https://flespi.io/docs/#/gw/calculators/get_calcs_calcs_selector_logs) |
| [List calculators](actions/list-calculators.md) | `GET /gw/calcs/all` | [docs](https://flespi.io/docs/#/gw/calculators/get_calcs_calcs_selector) |
| [List CDNs](actions/list-cdns.md) | `GET /storage/cdns/all` | [docs](https://flespi.io/docs/#/storage/cdns/get_cdns_cdn_selector) |
| [List channel idents](actions/list-channel-idents.md) | `GET /gw/channels/all/idents/all` | [docs](https://flespi.io/docs/#/gw/channels/get_channels_ch_selector_idents_channel_ident_selector) |
| [List channel logs](actions/list-channel-logs.md) | `GET /gw/channels/all/logs` | [docs](https://flespi.io/docs/#/gw/channels/get_channels_ch_selector_logs) |
| [List channel messages](actions/list-channel-messages.md) | `GET /gw/channels/all/messages` | [docs](https://flespi.io/docs/#/gw/channels/get_channels_ch_selector_messages) |
| [List channel protocol device types](actions/list-channel-protocol-device-types.md) | `GET /gw/channel-protocols/all/device-types/all` | [docs](https://flespi.io/docs/#/gw/channel-protocols/get_channel_protocols_channel_protocols_selector_device_types_devtypes_selector) |
| [List channel protocols](actions/list-channel-protocols.md) | `GET /gw/channel-protocols/all` | [docs](https://flespi.io/docs/#/gw/channel-protocols/get_channel_protocols_channel_protocols_selector) |
| [List channels](actions/list-channels.md) | `GET /gw/channels/all` | [docs](https://flespi.io/docs/#/gw/channels/get_channels_ch_selector) |
| [List containers](actions/list-containers.md) | `GET /storage/containers/all` | [docs](https://flespi.io/docs/#/storage/containers/get_containers_container_selector) |
| [List device command queue](actions/list-device-command-queue.md) | `GET /gw/devices/all/commands-queue/all` | [docs](https://flespi.io/docs/#/gw/devices/get_devices_dev_selector_commands_queue_devices_commands_queue_selector) |
| [List device connections](actions/list-device-connections.md) | `GET /gw/devices/all/connections/all` | [docs](https://flespi.io/docs/#/gw/devices/get_devices_dev_selector_connections_conn_selector) |
| [List device logs](actions/list-device-logs.md) | `GET /gw/devices/all/logs` | [docs](https://flespi.io/docs/#/gw/devices/get_devices_dev_selector_logs) |
| [List device telemetry](actions/list-device-telemetry.md) | `GET /gw/devices/all/telemetry/all` | [docs](https://flespi.io/docs/#/gw/devices/get_devices_dev_selector_telemetry_telemetry_selector) |
| [List devices](actions/list-devices.md) | `GET /gw/devices/all` | [docs](https://flespi.io/docs/#/gw/devices/get_devices_dev_selector) |
| [List expression functions](actions/list-expression-functions.md) | `GET /storage/expressions/functions` | [docs](https://flespi.io/docs/#/storage/expressions/get_expressions_functions) |
| [List geofence logs](actions/list-geofence-logs.md) | `GET /gw/geofences/all/logs` | [docs](https://flespi.io/docs/#/gw/geofences/get_geofences_geofences_selector_logs) |
| [List geofences](actions/list-geofences.md) | `GET /gw/geofences/all` | [docs](https://flespi.io/docs/#/gw/geofences/get_geofences_geofences_selector) |
| [List group logs](actions/list-group-logs.md) | `GET /gw/groups/all/logs` | [docs](https://flespi.io/docs/#/gw/groups/get_groups_groups_selector_logs) |
| [List groups](actions/list-groups.md) | `GET /gw/groups/all` | [docs](https://flespi.io/docs/#/gw/groups/get_groups_groups_selector) |
| [List modem logs](actions/list-modem-logs.md) | `GET /gw/modems/all/logs` | [docs](https://flespi.io/docs/#/gw/modems/get_modems_modems_selector_logs) |
| [List modems](actions/list-modems.md) | `GET /gw/modems/all` | [docs](https://flespi.io/docs/#/gw/modems/get_modems_modems_selector) |
| [List MQTT retained messages](actions/list-mqtt-retained-messages.md) | `GET /mqtt/messages/all` | [docs](https://flespi.io/docs/#/mqtt/messages/get_messages_messages_selector) |
| [List MQTT sessions](actions/list-mqtt-sessions.md) | `GET /mqtt/sessions/all` | [docs](https://flespi.io/docs/#/mqtt/sessions/get_sessions_sessions_selector) |
| [List plugin logs](actions/list-plugin-logs.md) | `GET /gw/plugins/all/logs` | [docs](https://flespi.io/docs/#/gw/plugins/get_plugins_plugins_selector_logs) |
| [List plugins](actions/list-plugins.md) | `GET /gw/plugins/all` | [docs](https://flespi.io/docs/#/gw/plugins/get_plugins_plugins_selector) |
| [List stream logs](actions/list-stream-logs.md) | `GET /gw/streams/all/logs` | [docs](https://flespi.io/docs/#/gw/streams/get_streams_streams_selector_logs) |
| [List streams](actions/list-streams.md) | `GET /gw/streams/all` | [docs](https://flespi.io/docs/#/gw/streams/get_streams_streams_selector) |
| [List webhooks](actions/list-webhooks.md) | `GET /gw/webhooks/all` | [docs](https://flespi.io/docs/#/gw/webhooks/get_webhooks_webhooks_selector) |
| [Update email stored in the flespi profile](actions/update-auth-email-update.md) | `PUT /auth/email/update` | [docs](https://flespi.io/docs/) |
| [Update profile password](actions/update-auth-password.md) | `PUT /auth/password` | [docs](https://flespi.io/docs/) |
| [Modify asset properties](actions/update-gw-assets-assets-selector.md) | `PUT /gw/assets/{assets.selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-gw-assets-assets-selector2.md) | `PATCH /gw/assets/{assets.selector}` | [docs](https://flespi.io/docs/) |
| [Update calculator configuration](actions/update-gw-calcs-calcs-selector.md) | `PUT /gw/calcs/{calcs.selector}` | [docs](https://flespi.io/docs/) |
| [Modify asset data for calc](actions/update-gw-calcs-calcs-selector-assets-calc-assets-selector.md) | `PUT /gw/calcs/{calcs.selector}/assets/{calc.assets.selector}` | [docs](https://flespi.io/docs/) |
| [Modify configuration of device assignment to calculator](actions/update-gw-calcs-calcs-selector-devices-calc-devices-selector.md) | `PUT /gw/calcs/{calcs.selector}/devices/{calc.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Attach custom parameters to calculated device interval](actions/update-gw-calcs-calcs-selector-devices-calc-devices-selector-intervals-calc-device-intervals-selector-put.md) | `PUT /gw/calcs/{calcs.selector}/devices/{calc.devices.selector}/intervals/{calc.device.intervals.selector.put}` | [docs](https://flespi.io/docs/) |
| [Modify geofence data for calc](actions/update-gw-calcs-calcs-selector-geofences-calc-geofences-selector.md) | `PUT /gw/calcs/{calcs.selector}/geofences/{calc.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Update assignment of group of devices to calculator](actions/update-gw-calcs-calcs-selector-groups-calc-groups-selector.md) | `PUT /gw/calcs/{calcs.selector}/groups/{calc.groups.selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-gw-calcs-calcs-selector2.md) | `PATCH /gw/calcs/{calcs.selector}` | [docs](https://flespi.io/docs/) |
| [Modify channels properties](actions/update-gw-channels-ch-selector.md) | `PUT /gw/channels/{ch-selector}` | [docs](https://flespi.io/docs/) |
| [Move channel between subaccounts](actions/update-gw-channels-ch-selector-cid.md) | `PUT /gw/channels/{ch-selector}/cid` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-gw-channels-ch-selector2.md) | `PATCH /gw/channels/{ch-selector}` | [docs](https://flespi.io/docs/) |
| [Modify device properties](actions/update-gw-devices-dev-selector.md) | `PUT /gw/devices/{dev-selector}` | [docs](https://flespi.io/docs/) |
| [Move device between subaccounts](actions/update-gw-devices-dev-selector-cid.md) | `PUT /gw/devices/{dev-selector}/cid` | [docs](https://flespi.io/docs/) |
| [Attach own data to media file](actions/update-gw-devices-dev-selector-media.md) | `PUT /gw/devices/{dev-selector}/media` | [docs](https://flespi.io/docs/) |
| [Request device to apply new setting value](actions/update-gw-devices-dev-selector-settings-sett-selector.md) | `PUT /gw/devices/{dev-selector}/settings/{sett-selector}` | [docs](https://flespi.io/docs/) |
| [Modify fields inside device configuration](actions/update-gw-devices-dev-selector2.md) | `PATCH /gw/devices/{dev-selector}` | [docs](https://flespi.io/docs/) |
| [Modify geofence properties](actions/update-gw-geofences-geofences-selector.md) | `PUT /gw/geofences/{geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-gw-geofences-geofences-selector2.md) | `PATCH /gw/geofences/{geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Modify group properties](actions/update-gw-groups-groups-selector.md) | `PUT /gw/groups/{groups.selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-gw-groups-groups-selector2.md) | `PATCH /gw/groups/{groups.selector}` | [docs](https://flespi.io/docs/) |
| [Update modem configuration](actions/update-gw-modems-modem-selector.md) | `PUT /gw/modems/{modem-selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-gw-modems-modem-selector2.md) | `PATCH /gw/modems/{modem-selector}` | [docs](https://flespi.io/docs/) |
| [Modify plugin properties](actions/update-gw-plugins-plugin-selector.md) | `PUT /gw/plugins/{plugin.selector}` | [docs](https://flespi.io/docs/) |
| [Modify full device data for plugin](actions/update-gw-plugins-plugin-selector-devices-plugin-devices-selector.md) | `PUT /gw/plugins/{plugin.selector}/devices/{plugin.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Modify subset of device data for plugin](actions/update-gw-plugins-plugin-selector-devices-plugin-devices-selector2.md) | `PATCH /gw/plugins/{plugin.selector}/devices/{plugin.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Modify geofence data for plugin](actions/update-gw-plugins-plugin-selector-geofences-plugin-geofences-selector.md) | `PUT /gw/plugins/{plugin.selector}/geofences/{plugin.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Update assignment of group of devices to plugin](actions/update-gw-plugins-plugin-selector-groups-plugin-groups-selector.md) | `PUT /gw/plugins/{plugin.selector}/groups/{plugin.groups.selector}` | [docs](https://flespi.io/docs/) |
| [Modify fields inside plugin configuration](actions/update-gw-plugins-plugin-selector2.md) | `PATCH /gw/plugins/{plugin.selector}` | [docs](https://flespi.io/docs/) |
| [Modify stream properties](actions/update-gw-streams-stream-selector.md) | `PUT /gw/streams/{stream.selector}` | [docs](https://flespi.io/docs/) |
| [Modify device data for stream](actions/update-gw-streams-stream-selector-devices-stream-devices-selector.md) | `PUT /gw/streams/{stream.selector}/devices/{stream.devices.selector}` | [docs](https://flespi.io/docs/) |
| [Modify geofence data for stream](actions/update-gw-streams-stream-selector-geofences-stream-geofences-selector.md) | `PUT /gw/streams/{stream.selector}/geofences/{stream.geofences.selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-gw-streams-stream-selector2.md) | `PATCH /gw/streams/{stream.selector}` | [docs](https://flespi.io/docs/) |
| [Update customer billing configuration](actions/update-platform-billing.md) | `PUT /platform/billing` | [docs](https://flespi.io/docs/) |
| [Modify your customer account information](actions/update-platform-customer.md) | `PUT /platform/customer` | [docs](https://flespi.io/docs/) |
| [Indicate that you are typing reply in flespi support chat.](actions/update-platform-customer-chat.md) | `PUT /platform/customer/chat` | [docs](https://flespi.io/docs/) |
| [Patch your customer account information](actions/update-platform-customer2.md) | `PATCH /platform/customer` | [docs](https://flespi.io/docs/) |
| [Update grant configuration](actions/update-platform-grants-grants-selector.md) | `PUT /platform/grants/{grants-selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-platform-grants-grants-selector2.md) | `PATCH /platform/grants/{grants-selector}` | [docs](https://flespi.io/docs/) |
| [Update Identity Provider configuration](actions/update-platform-identity-providers-identity-provider-selector.md) | `PUT /platform/identity-providers/{identity-provider-selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-platform-identity-providers-identity-provider-selector2.md) | `PATCH /platform/identity-providers/{identity-provider-selector}` | [docs](https://flespi.io/docs/) |
| [Update subaccount limit configuration](actions/update-platform-limits-limits-selector.md) | `PUT /platform/limits/{limits-selector}` | [docs](https://flespi.io/docs/) |
| [Update subaccount limit configuration](actions/update-platform-limits-limits-selector2.md) | `PATCH /platform/limits/{limits-selector}` | [docs](https://flespi.io/docs/) |
| [Update realm configuration](actions/update-platform-realms-realm-selector.md) | `PUT /platform/realms/{realm-selector}` | [docs](https://flespi.io/docs/) |
| [Modify the binding of Identity Provider to realms](actions/update-platform-realms-realm-selector-identity-providers-realm-identity-provider-selector.md) | `PUT /platform/realms/{realm-selector}/identity-providers/{realm-identity-provider-selector}` | [docs](https://flespi.io/docs/) |
| [Modify realm role](actions/update-platform-realms-realm-selector-roles-role-selector.md) | `PUT /platform/realms/{realm-selector}/roles/{role-selector}` | [docs](https://flespi.io/docs/) |
| [Modify realm role](actions/update-platform-realms-realm-selector-roles-role-selector2.md) | `PATCH /platform/realms/{realm-selector}/roles/{role-selector}` | [docs](https://flespi.io/docs/) |
| [Modify realm user](actions/update-platform-realms-realm-selector-users-user-selector.md) | `PUT /platform/realms/{realm-selector}/users/{user-selector}` | [docs](https://flespi.io/docs/) |
| [Modify realm user](actions/update-platform-realms-realm-selector-users-user-selector2.md) | `PATCH /platform/realms/{realm-selector}/users/{user-selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-platform-realms-realm-selector2.md) | `PATCH /platform/realms/{realm-selector}` | [docs](https://flespi.io/docs/) |
| [Update subaccount configuration](actions/update-platform-subaccounts-subaccounts-selector.md) | `PUT /platform/subaccounts/{subaccounts-selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-platform-subaccounts-subaccounts-selector2.md) | `PATCH /platform/subaccounts/{subaccounts-selector}` | [docs](https://flespi.io/docs/) |
| [Update token configuration](actions/update-platform-tokens-tokens-selector.md) | `PUT /platform/tokens/{tokens-selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-platform-tokens-tokens-selector2.md) | `PATCH /platform/tokens/{tokens-selector}` | [docs](https://flespi.io/docs/) |
| [Update webhook configuration](actions/update-platform-webhooks-webhooks-selector.md) | `PUT /platform/webhooks/{webhooks-selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-platform-webhooks-webhooks-selector2.md) | `PATCH /platform/webhooks/{webhooks-selector}` | [docs](https://flespi.io/docs/) |
| [Set realm user password](actions/update-realm-realm-public-id-user.md) | `PUT /realm/{realm-public-id}/user` | [docs](https://flespi.io/docs/) |
| [Modify CDN properties](actions/update-storage-cdns-cdn-selector.md) | `PUT /storage/cdns/{cdn-selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-storage-cdns-cdn-selector2.md) | `PATCH /storage/cdns/{cdn-selector}` | [docs](https://flespi.io/docs/) |
| [Modify container properties](actions/update-storage-containers-container-selector.md) | `PUT /storage/containers/{container-selector}` | [docs](https://flespi.io/docs/) |
| [Patch item properties](actions/update-storage-containers-container-selector2.md) | `PATCH /storage/containers/{container-selector}` | [docs](https://flespi.io/docs/) |
