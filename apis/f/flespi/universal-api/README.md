# <img src="https://images.mindcloud.co/apps/icons/flespi-icon_1776706125472.png" alt="Flespi logo" width="28" height="28"> Flespi: Universal API

Flespi is a telematics and IoT backend platform with REST APIs for device connectivity, gateway resources, storage, MQTT broker operations, account resources, authentication realms, and AI tools.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/flespi/latest
- **Actions:** 365
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://flespi.com
- **Vendor API docs:** https://flespi.com/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List devices](actions/list-devices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (365)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Accept/deny flespi account rules](actions/create-auth-account-confirm.md) | POST |  |
| [Register new flespi account by email](actions/create-auth-account-register.md) | POST |  |

### Ai Log

| Action | Method | Description |
| --- | --- | --- |
| [Get AI logs](actions/get-ai-logs.md) | GET |  |

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [List assets](actions/list-assets.md) | GET |  |

### Asset Log

| Action | Method | Description |
| --- | --- | --- |
| [List asset logs](actions/list-asset-logs.md) | GET |  |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create new asset](actions/create-gw-assets.md) | POST |  |
| [Post Gw Assets Intervals](actions/create-gw-assets-assets-selector-intervals.md) | POST |  |
| [Calculate intervals from asset logs](actions/create-gw-assets-assets-selector-logs-calculate.md) | POST |  |
| [Delete selected assets](actions/delete-gw-assets-assets-selector.md) | DELETE |  |
| [List available assets](actions/get-gw-assets-assets-selector.md) | GET |  |
| [Get Gw Assets Intervals](actions/get-gw-assets-assets-selector-intervals.md) | GET |  |
| [Retrieve asset logs](actions/get-gw-assets-assets-selector-logs.md) | GET |  |
| [Modify asset properties](actions/update-gw-assets-assets-selector.md) | PUT |  |
| [Patch item properties](actions/update-gw-assets-assets-selector2.md) | PUT |  |

### Billing

| Action | Method | Description |
| --- | --- | --- |
| [Attempt to charge invoice](actions/create-platform-billing-invoices-invoices-selector-charge.md) | POST |  |
| [Retrieve customer billing information](actions/get-platform-billing.md) | GET |  |
| [Retrieve issued invoices](actions/get-platform-billing-invoices-invoices-selector.md) | GET |  |
| [Fetch payment portal link.](actions/get-platform-billing-payment-portal.md) | GET |  |
| [Update customer billing configuration](actions/update-platform-billing.md) | PUT |  |

### Calcs

| Action | Method | Description |
| --- | --- | --- |
| [Create calculator configuration](actions/create-gw-calcs.md) | POST |  |
| [Assign assets to calc](actions/create-gw-calcs-calcs-selector-assets-calc-assets-selector.md) | POST |  |
| [Split calculated intervals on a higher level intervals](actions/create-gw-calcs-calcs-selector-devices-calc-devices-selector-calculate.md) | POST |  |
| [Recalculate assigned device intervals](actions/create-gw-calcs-calcs-selector-devices-calc-devices-selector-recalculate.md) | POST |  |
| [Assign devices to calculator](actions/create-gw-calcs-calcs-selector-devices-dev-selector.md) | POST |  |
| [Assign geofences to calc](actions/create-gw-calcs-calcs-selector-geofences-calc-geofences-selector.md) | POST |  |
| [Assign a group of devices to a calculator](actions/create-gw-calcs-calcs-selector-groups-calc-groups-selector.md) | POST |  |
| [Calculate intervals from calculator logs](actions/create-gw-calcs-calcs-selector-logs-calculate.md) | POST |  |
| [Delete calculator and all calculated intervals from assigned devices](actions/delete-gw-calcs-calcs-selector.md) | DELETE |  |
| [Unassign assets from calc](actions/delete-gw-calcs-calcs-selector-assets-calc-assets-selector.md) | DELETE |  |
| [Unassign device from calculator](actions/delete-gw-calcs-calcs-selector-devices-calc-devices-selector.md) | DELETE |  |
| [Unassign geofences from calc](actions/delete-gw-calcs-calcs-selector-geofences-calc-geofences-selector.md) | DELETE |  |
| [Unassign a group from calculator](actions/delete-gw-calcs-calcs-selector-groups-calc-groups-selector.md) | DELETE |  |
| [Retrieve calculator configuration](actions/get-gw-calcs-calcs-selector.md) | GET |  |
| [Retrieve assets in calc](actions/get-gw-calcs-calcs-selector-assets-calc-assets-selector.md) | GET |  |
| [List devices assigned to calculator](actions/get-gw-calcs-calcs-selector-devices-calc-devices-selector.md) | GET |  |
| [Retrieve calculated device intervals](actions/get-gw-calcs-calcs-selector-devices-calc-devices-selector-intervals-calc-device-intervals-selector.md) | GET |  |
| [Retrieve geofences in calc](actions/get-gw-calcs-calcs-selector-geofences-calc-geofences-selector.md) | GET |  |
| [Fetch groups assigned to the calculator](actions/get-gw-calcs-calcs-selector-groups-calc-groups-selector.md) | GET |  |
| [Retrieve calculator logs](actions/get-gw-calcs-calcs-selector-logs.md) | GET |  |
| [Update calculator configuration](actions/update-gw-calcs-calcs-selector.md) | PUT |  |
| [Modify asset data for calc](actions/update-gw-calcs-calcs-selector-assets-calc-assets-selector.md) | PUT |  |
| [Modify configuration of device assignment to calculator](actions/update-gw-calcs-calcs-selector-devices-calc-devices-selector.md) | PUT |  |
| [Attach custom parameters to calculated device interval](actions/update-gw-calcs-calcs-selector-devices-calc-devices-selector-intervals-calc-device-intervals-selector-put.md) | PUT |  |
| [Modify geofence data for calc](actions/update-gw-calcs-calcs-selector-geofences-calc-geofences-selector.md) | PUT |  |
| [Update assignment of group of devices to calculator](actions/update-gw-calcs-calcs-selector-groups-calc-groups-selector.md) | PUT |  |
| [Patch item properties](actions/update-gw-calcs-calcs-selector2.md) | PUT |  |

### Calculator

| Action | Method | Description |
| --- | --- | --- |
| [List calculators](actions/list-calculators.md) | GET |  |

### Calculator Log

| Action | Method | Description |
| --- | --- | --- |
| [List calculator logs](actions/list-calculator-logs.md) | GET |  |

### Callback

| Action | Method | Description |
| --- | --- | --- |
| [Identity provider callback](actions/get-auth-callback.md) | GET |  |
| [Identity provider proxy callback](actions/get-auth-callback-proxy.md) | GET |  |

### Cdn

| Action | Method | Description |
| --- | --- | --- |
| [List CDNs](actions/list-cdns.md) | GET |  |

### Cdns

| Action | Method | Description |
| --- | --- | --- |
| [Create new CDN](actions/create-storage-cdns.md) | POST |  |
| [Upload files to CDN](actions/create-storage-cdns-cdn-selector-files.md) | POST |  |
| [Calculate intervals from CDN logs](actions/create-storage-cdns-cdn-selector-logs-calculate.md) | POST |  |
| [Delete selected CDNs](actions/delete-storage-cdns-cdn-selector.md) | DELETE |  |
| [Delete files from CDN](actions/delete-storage-cdns-cdn-selector-files.md) | DELETE |  |
| [List available CDNs](actions/get-storage-cdns-cdn-selector.md) | GET |  |
| [List CDN files](actions/get-storage-cdns-cdn-selector-files.md) | GET |  |
| [Retrieve CDN logs](actions/get-storage-cdns-cdn-selector-logs.md) | GET |  |
| [Modify CDN properties](actions/update-storage-cdns-cdn-selector.md) | PUT |  |
| [Patch item properties](actions/update-storage-cdns-cdn-selector2.md) | PUT |  |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List channels](actions/list-channels.md) | GET |  |

### Channel Ident

| Action | Method | Description |
| --- | --- | --- |
| [List channel idents](actions/list-channel-idents.md) | GET |  |

### Channel Log

| Action | Method | Description |
| --- | --- | --- |
| [List channel logs](actions/list-channel-logs.md) | GET |  |

### Channel Message

| Action | Method | Description |
| --- | --- | --- |
| [List channel messages](actions/list-channel-messages.md) | GET |  |

### Channel Protocol

| Action | Method | Description |
| --- | --- | --- |
| [List channel protocols](actions/list-channel-protocols.md) | GET |  |

### Channel Protocols

| Action | Method | Description |
| --- | --- | --- |
| [Fetch available channel protocols](actions/get-gw-channel-protocols-channel-protocols-selector.md) | GET |  |
| [Get available device types withing selected channel protocols](actions/get-gw-channel-protocols-channel-protocols-selector-device-types-devtypes-selector.md) | GET |  |

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Create new channel](actions/create-gw-channels.md) | POST |  |
| [Calculate intervals from channel logs](actions/create-gw-channels-ch-selector-logs-calculate.md) | POST |  |
| [Delete channels](actions/delete-gw-channels-ch-selector.md) | DELETE |  |
| [Close TCP connections](actions/delete-gw-channels-ch-selector-connections-conn-selector.md) | DELETE |  |
| [Delete messages from channel buffer](actions/delete-gw-channels-ch-selector-messages.md) | DELETE |  |
| [List available channels](actions/get-gw-channels-ch-selector.md) | GET |  |
| [List active channel TCP connections](actions/get-gw-channels-ch-selector-connections-conn-selector.md) | GET |  |
| [Retrieve raw traffic for ident](actions/get-gw-channels-ch-selector-idents-ch-ident-selector-packets.md) | GET |  |
| [List idents reported to the channel](actions/get-gw-channels-ch-selector-idents-channel-ident-selector.md) | GET |  |
| [Retrieve channel logs](actions/get-gw-channels-ch-selector-logs.md) | GET |  |
| [Read messages from channel buffer](actions/get-gw-channels-ch-selector-messages.md) | GET |  |
| [Modify channels properties](actions/update-gw-channels-ch-selector.md) | PUT |  |
| [Move channel between subaccounts](actions/update-gw-channels-ch-selector-cid.md) | PUT |  |
| [Patch item properties](actions/update-gw-channels-ch-selector2.md) | PUT |  |

### Confirm

| Action | Method | Description |
| --- | --- | --- |
| [Confirm realm user registration](actions/create-realm-realm-public-id-confirm.md) | POST |  |

### Container

| Action | Method | Description |
| --- | --- | --- |
| [List containers](actions/list-containers.md) | GET |  |

### Containers

| Action | Method | Description |
| --- | --- | --- |
| [Create new container](actions/create-storage-containers.md) | POST |  |
| [Split container messages into intervals](actions/create-storage-containers-container-selector-calculate.md) | POST |  |
| [Calculate intervals from container logs](actions/create-storage-containers-container-selector-logs-calculate.md) | POST |  |
| [Post messages to container](actions/create-storage-containers-container-selector-messages.md) | POST |  |
| [Delete selected containers](actions/delete-storage-containers-container-selector.md) | DELETE |  |
| [Delete messages from container](actions/delete-storage-containers-container-selector-messages.md) | DELETE |  |
| [List available containers](actions/get-storage-containers-container-selector.md) | GET |  |
| [Retrieve container logs](actions/get-storage-containers-container-selector-logs.md) | GET |  |
| [Retrieve messages from container](actions/get-storage-containers-container-selector-messages.md) | GET |  |
| [Modify container properties](actions/update-storage-containers-container-selector.md) | PUT |  |
| [Patch item properties](actions/update-storage-containers-container-selector2.md) | PUT |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Post message adressed to flespi support.](actions/create-platform-customer-chat.md) | POST |  |
| [Control AI assistant](actions/create-platform-customer-chat-ai-assistant.md) | POST |  |
| [Attach file to flespi support chat.](actions/create-platform-customer-chat-file.md) | POST |  |
| [Calculate intervals from customer logs](actions/create-platform-customer-logs-calculate.md) | POST |  |
| [Retrieve customer account information](actions/get-platform-customer.md) | GET |  |
| [Retrieve chat communication history between flespi support and customer.](actions/get-platform-customer-chat.md) | GET |  |
| [Retrieve knowledge links](actions/get-platform-customer-chat-knowledge.md) | GET |  |
| [Get platform log records.](actions/get-platform-customer-logs.md) | GET |  |
| [Get platform statistics records.](actions/get-platform-customer-statistics.md) | GET |  |
| [Newslist unsubscription callback](actions/get-platform-customer-unsubscribe.md) | GET |  |
| [Modify your customer account information](actions/update-platform-customer.md) | PUT |  |
| [Indicate that you are typing reply in flespi support chat.](actions/update-platform-customer-chat.md) | PUT |  |
| [Patch your customer account information](actions/update-platform-customer2.md) | PUT |  |

### Deleted

| Action | Method | Description |
| --- | --- | --- |
| [Calculate intervals from deleted item logs](actions/create-platform-deleted-deleted-selector-logs-calculate.md) | POST |  |
| [Try to restore deleted items.](actions/create-platform-deleted-deleted-selector-restore.md) | POST |  |
| [Get deleted items list. Deleted items are available for logs analyzer up to one month.](actions/get-platform-deleted-deleted-selector.md) | GET |  |
| [Get deleted item logs records.](actions/get-platform-deleted-deleted-selector-logs.md) | GET |  |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Get devices by selector](actions/get-devices-by-selector.md) | GET |  |
| [List devices](actions/list-devices.md) | GET |  |

### Device Command Queue Item

| Action | Method | Description |
| --- | --- | --- |
| [List device command queue](actions/list-device-command-queue.md) | GET |  |

### Device Connection

| Action | Method | Description |
| --- | --- | --- |
| [List device connections](actions/list-device-connections.md) | GET |  |

### Device Log

| Action | Method | Description |
| --- | --- | --- |
| [List device logs](actions/list-device-logs.md) | GET |  |

### Device Telemetry

| Action | Method | Description |
| --- | --- | --- |
| [List device telemetry](actions/list-device-telemetry.md) | GET |  |

### Device Type

| Action | Method | Description |
| --- | --- | --- |
| [List channel protocol device types](actions/list-channel-protocol-device-types.md) | GET |  |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Create new device](actions/create-gw-devices.md) | POST |  |
| [Split devices messages into intervals (run reports)](actions/create-gw-devices-dev-selector-calculate.md) | POST |  |
| [Send command to the connected device in real-time](actions/create-gw-devices-dev-selector-commands.md) | POST |  |
| [Schedule command execution](actions/create-gw-devices-dev-selector-commands-queue.md) | POST |  |
| [Assign geofences to device](actions/create-gw-devices-dev-selector-geofences-dev-geofences-selector.md) | POST |  |
| [Calculate intervals from device logs](actions/create-gw-devices-dev-selector-logs-calculate.md) | POST |  |
| [Upload media file to device](actions/create-gw-devices-dev-selector-media.md) | POST |  |
| [Register messages into device](actions/create-gw-devices-dev-selector-messages.md) | POST |  |
| [Send SMS command to the device in real-time](actions/create-gw-devices-dev-selector-sms.md) | POST |  |
| [Delete selected devices](actions/delete-gw-devices-dev-selector.md) | DELETE |  |
| [Remove command from queue](actions/delete-gw-devices-dev-selector-commands-queue-devices-commands-queue-selector.md) | DELETE |  |
| [Close TCP connections](actions/delete-gw-devices-dev-selector-connections-conn-selector.md) | DELETE |  |
| [Unassign geofences from device](actions/delete-gw-devices-dev-selector-geofences-dev-geofences-selector.md) | DELETE |  |
| [Delete media files](actions/delete-gw-devices-dev-selector-media.md) | DELETE |  |
| [Re-read setting value from the device or cancel setting update request](actions/delete-gw-devices-dev-selector-settings-sett-selector.md) | DELETE |  |
| [Delete device telemetry fields](actions/delete-gw-devices-dev-selector-telemetry-telemetry-selector.md) | DELETE |  |
| [Retrieve list of queued commands](actions/get-gw-devices-dev-selector-commands-queue-devices-commands-queue-selector.md) | GET |  |
| [Get executed or expired commands](actions/get-gw-devices-dev-selector-commands-result.md) | GET |  |
| [Get executed or expired command by its ID](actions/get-gw-devices-dev-selector-commands-result-command-id-selector.md) | GET |  |
| [List active TCP connections](actions/get-gw-devices-dev-selector-connections-conn-selector.md) | GET |  |
| [Retrieve geofences in device](actions/get-gw-devices-dev-selector-geofences-dev-geofences-selector.md) | GET |  |
| [Retrieve device logs](actions/get-gw-devices-dev-selector-logs.md) | GET |  |
| [List device media files](actions/get-gw-devices-dev-selector-media.md) | GET |  |
| [Retrieve messages stored by the device](actions/get-gw-devices-dev-selector-messages.md) | GET |  |
| [Retrieve raw device traffic](actions/get-gw-devices-dev-selector-packets.md) | GET |  |
| [Retrieve device settings](actions/get-gw-devices-dev-selector-settings-sett-selector.md) | GET |  |
| [Generate SMS message text for the command](actions/get-gw-devices-dev-selector-sms.md) | GET |  |
| [Retrieve device telemetry](actions/get-gw-devices-dev-selector-telemetry-telemetry-selector.md) | GET |  |
| [Modify device properties](actions/update-gw-devices-dev-selector.md) | PUT |  |
| [Move device between subaccounts](actions/update-gw-devices-dev-selector-cid.md) | PUT |  |
| [Attach own data to media file](actions/update-gw-devices-dev-selector-media.md) | PUT |  |
| [Request device to apply new setting value](actions/update-gw-devices-dev-selector-settings-sett-selector.md) | PUT |  |
| [Modify fields inside device configuration](actions/update-gw-devices-dev-selector2.md) | PUT |  |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Email verification callback](actions/create-auth-email-confirm.md) | POST |  |
| [Email verification fallback](actions/create-auth-email-revert.md) | POST |  |
| [Update email stored in the flespi profile](actions/update-auth-email-update.md) | PUT |  |

### Expression Function

| Action | Method | Description |
| --- | --- | --- |
| [List expression functions](actions/list-expression-functions.md) | GET |  |

### Expressions

| Action | Method | Description |
| --- | --- | --- |
| [Test expression evaluation](actions/create-storage-expressions-test.md) | POST |  |

### Geofence

| Action | Method | Description |
| --- | --- | --- |
| [List geofences](actions/list-geofences.md) | GET |  |

### Geofence Log

| Action | Method | Description |
| --- | --- | --- |
| [List geofence logs](actions/list-geofence-logs.md) | GET |  |

### Geofences

| Action | Method | Description |
| --- | --- | --- |
| [Create new geofence](actions/create-gw-geofences.md) | POST |  |
| [Calculate intervals from geofence logs](actions/create-gw-geofences-geofences-selector-logs-calculate.md) | POST |  |
| [Delete selected geofences](actions/delete-gw-geofences-geofences-selector.md) | DELETE |  |
| [List available geofences](actions/get-gw-geofences-geofences-selector.md) | GET |  |
| [Test if the point is inside geofences.](actions/get-gw-geofences-geofences-selector-hittest.md) | GET |  |
| [Retrieve geofence logs](actions/get-gw-geofences-geofences-selector-logs.md) | GET |  |
| [Modify geofence properties](actions/update-gw-geofences-geofences-selector.md) | PUT |  |
| [Patch item properties](actions/update-gw-geofences-geofences-selector2.md) | PUT |  |

### Grantors

| Action | Method | Description |
| --- | --- | --- |
| [Delete the grantors](actions/delete-platform-grantors-grants-selector.md) | DELETE |  |
| [Retrieve grantors](actions/get-platform-grantors-grants-selector.md) | GET |  |

### Grants

| Action | Method | Description |
| --- | --- | --- |
| [Create grant](actions/create-platform-grants.md) | POST |  |
| [Calculate intervals from grant logs](actions/create-platform-grants-grants-selector-logs-calculate.md) | POST |  |
| [Grant items access to subaccount](actions/create-platform-grants-grants-selector-subaccounts-grant-subaccounts-selector.md) | POST |  |
| [Delete grant](actions/delete-platform-grants-grants-selector.md) | DELETE |  |
| [Revoke items access for subaccount](actions/delete-platform-grants-grants-selector-subaccounts-grant-subaccounts-selector.md) | DELETE |  |
| [Retrieve grants](actions/get-platform-grants-grants-selector.md) | GET |  |
| [Retrieve grant logs](actions/get-platform-grants-grants-selector-logs.md) | GET |  |
| [Get subaccounts to which items access is granted](actions/get-platform-grants-grants-selector-subaccounts-grant-subaccounts-selector.md) | GET |  |
| [Update grant configuration](actions/update-platform-grants-grants-selector.md) | PUT |  |
| [Patch item properties](actions/update-platform-grants-grants-selector2.md) | PUT |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List groups](actions/list-groups.md) | GET |  |

### Group Log

| Action | Method | Description |
| --- | --- | --- |
| [List group logs](actions/list-group-logs.md) | GET |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create new group](actions/create-gw-groups.md) | POST |  |
| [Assign assets to group](actions/create-gw-groups-groups-selector-assets-group-assets-selector.md) | POST |  |
| [Assign devices to group](actions/create-gw-groups-groups-selector-devices-group-devices-selector.md) | POST |  |
| [Assign geofences to group](actions/create-gw-groups-groups-selector-geofences-group-geofences-selector.md) | POST |  |
| [Calculate intervals from group logs](actions/create-gw-groups-groups-selector-logs-calculate.md) | POST |  |
| [Delete selected groups](actions/delete-gw-groups-groups-selector.md) | DELETE |  |
| [Unassign assets from group](actions/delete-gw-groups-groups-selector-assets-group-assets-selector.md) | DELETE |  |
| [Unassign devices from group](actions/delete-gw-groups-groups-selector-devices-group-devices-selector.md) | DELETE |  |
| [Unassign geofences from group](actions/delete-gw-groups-groups-selector-geofences-group-geofences-selector.md) | DELETE |  |
| [List available groups](actions/get-gw-groups-groups-selector.md) | GET |  |
| [Retrieve assets in group](actions/get-gw-groups-groups-selector-assets-group-assets-selector.md) | GET |  |
| [Retrieve devices in group](actions/get-gw-groups-groups-selector-devices-group-devices-selector.md) | GET |  |
| [Retrieve geofences in group](actions/get-gw-groups-groups-selector-geofences-group-geofences-selector.md) | GET |  |
| [Retrieve group logs](actions/get-gw-groups-groups-selector-logs.md) | GET |  |
| [Modify group properties](actions/update-gw-groups-groups-selector.md) | PUT |  |
| [Patch item properties](actions/update-gw-groups-groups-selector2.md) | PUT |  |

### Identity Providers

| Action | Method | Description |
| --- | --- | --- |
| [Create Identity Provider](actions/create-platform-identity-providers.md) | POST |  |
| [Calculate intervals from identity provider logs](actions/create-platform-identity-providers-identity-provider-selector-logs-calculate.md) | POST |  |
| [Delete Identity Providers](actions/delete-platform-identity-providers-identity-provider-selector.md) | DELETE |  |
| [Retrieve Identity Provider](actions/get-platform-identity-providers-identity-provider-selector.md) | GET |  |
| [Retrieve identity provider logs](actions/get-platform-identity-providers-identity-provider-selector-logs.md) | GET |  |
| [Retrieve identity providers linked with realm](actions/get-realm-realm-public-id-identity-providers.md) | GET |  |
| [Retrieve identity provider log in link](actions/get-realm-realm-public-id-identity-providers-identity-provider-id-login.md) | GET |  |
| [Update Identity Provider configuration](actions/update-platform-identity-providers-identity-provider-selector.md) | PUT |  |
| [Patch item properties](actions/update-platform-identity-providers-identity-provider-selector2.md) | PUT |  |

### Info

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve token information](actions/get-auth-info.md) | GET |  |
| [Retrieve realm information](actions/get-realm-realm-public-id-info.md) | GET |  |

### Limits

| Action | Method | Description |
| --- | --- | --- |
| [Create subaccount limit](actions/create-platform-limits.md) | POST |  |
| [Calculate intervals from limit logs](actions/create-platform-limits-limits-selector-logs-calculate.md) | POST |  |
| [Delete subaccount limits](actions/delete-platform-limits-limits-selector.md) | DELETE |  |
| [Retrieve subaccount limits](actions/get-platform-limits-limits-selector.md) | GET |  |
| [Retrieve subaccount limit logs](actions/get-platform-limits-limits-selector-logs.md) | GET |  |
| [Update subaccount limit configuration](actions/update-platform-limits-limits-selector.md) | PUT |  |
| [Update subaccount limit configuration](actions/update-platform-limits-limits-selector2.md) | PUT |  |

### Login

| Action | Method | Description |
| --- | --- | --- |
| [Login to the flespi panel using email and password](actions/create-auth-login-credentials.md) | POST |  |
| [Request passwordless login link](actions/create-auth-login-passwordless.md) | POST |  |
| [Passwordless login confirmation](actions/create-auth-login-passwordless-confirm.md) | POST |  |
| [Authorize realm user](actions/create-realm-realm-public-id-login.md) | POST |  |

### Logs

| Action | Method | Description |
| --- | --- | --- |
| [Calculate intervals from AI logs](actions/create-ai-logs-calculate.md) | POST |  |
| [Calculate intervals from MQTT broker logs](actions/create-mqtt-logs-calculate.md) | POST |  |

### Mcp

| Action | Method | Description |
| --- | --- | --- |
| [MCP server for development agents](actions/create-ai-mcp-develop.md) | POST |  |
| [MCP server for support agents](actions/create-ai-mcp-support.md) | POST |  |

### Mcp Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get AI development MCP schema](actions/get-ai-development-mcp-schema.md) | GET |  |
| [Get AI support MCP schema](actions/get-ai-support-mcp-schema.md) | GET |  |

### Message Parameters

| Action | Method | Description |
| --- | --- | --- |
| [Fetch standard message parameters](actions/get-gw-message-parameters-message-parameter-selector.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Publish MQTT message](actions/create-mqtt-messages.md) | POST |  |
| [Delete retained MQTT messages](actions/delete-mqtt-messages-messages-selector.md) | DELETE |  |
| [Get retained messages](actions/get-mqtt-messages-messages-selector.md) | GET |  |

### Modem

| Action | Method | Description |
| --- | --- | --- |
| [List modems](actions/list-modems.md) | GET |  |

### Modem Log

| Action | Method | Description |
| --- | --- | --- |
| [List modem logs](actions/list-modem-logs.md) | GET |  |

### Modems

| Action | Method | Description |
| --- | --- | --- |
| [Create modem](actions/create-gw-modems.md) | POST |  |
| [Calculate intervals from modem logs](actions/create-gw-modems-modem-selector-logs-calculate.md) | POST |  |
| [Delete modem](actions/delete-gw-modems-modem-selector.md) | DELETE |  |
| [Retrieve modems](actions/get-gw-modems-modem-selector.md) | GET |  |
| [Retrieve modem logs](actions/get-gw-modems-modem-selector-logs.md) | GET |  |
| [Update modem configuration](actions/update-gw-modems-modem-selector.md) | PUT |  |
| [Patch item properties](actions/update-gw-modems-modem-selector2.md) | PUT |  |

### Mqtt Log

| Action | Method | Description |
| --- | --- | --- |
| [Get MQTT logs](actions/get-mqtt-logs.md) | GET |  |

### Mqtt Retained Message

| Action | Method | Description |
| --- | --- | --- |
| [List MQTT retained messages](actions/list-mqtt-retained-messages.md) | GET |  |

### Mqtt Session

| Action | Method | Description |
| --- | --- | --- |
| [List MQTT sessions](actions/list-mqtt-sessions.md) | GET |  |

### Oauth

| Action | Method | Description |
| --- | --- | --- |
| [Detach selected OAuth profiles from flespi customer](actions/delete-platform-oauth-oauth-selector.md) | DELETE |  |
| [Link OAuth account to the flespi account](actions/get-auth-oauth-link.md) | GET |  |
| [Login and register to flespi](actions/get-auth-oauth-login.md) | GET |  |
| [List supported OAuth providers](actions/get-auth-oauth-providers.md) | GET |  |
| [Get customer's OAuth profiles](actions/get-platform-oauth-oauth-selector.md) | GET |  |

### Password

| Action | Method | Description |
| --- | --- | --- |
| [Update profile password](actions/update-auth-password.md) | PUT |  |

### Plugin

| Action | Method | Description |
| --- | --- | --- |
| [List plugins](actions/list-plugins.md) | GET |  |

### Plugin Log

| Action | Method | Description |
| --- | --- | --- |
| [List plugin logs](actions/list-plugin-logs.md) | GET |  |

### Plugin Types

| Action | Method | Description |
| --- | --- | --- |
| [Fetch available plugin types](actions/get-gw-plugin-types-plugin-types-selector.md) | GET |  |

### Plugins

| Action | Method | Description |
| --- | --- | --- |
| [Create new plugin](actions/create-gw-plugins.md) | POST |  |
| [Assign devices to plugin](actions/create-gw-plugins-plugin-selector-devices-plugin-devices-selector.md) | POST |  |
| [Assign geofences to plugin](actions/create-gw-plugins-plugin-selector-geofences-plugin-geofences-selector.md) | POST |  |
| [Assign a group of devices to a plugin](actions/create-gw-plugins-plugin-selector-groups-plugin-groups-selector.md) | POST |  |
| [Calculate intervals from plugin logs](actions/create-gw-plugins-plugin-selector-logs-calculate.md) | POST |  |
| [Delete selected plugins](actions/delete-gw-plugins-plugin-selector.md) | DELETE |  |
| [Unassign device from group](actions/delete-gw-plugins-plugin-selector-devices-plugin-devices-selector.md) | DELETE |  |
| [Unassign geofences from plugin](actions/delete-gw-plugins-plugin-selector-geofences-plugin-geofences-selector.md) | DELETE |  |
| [Unassign a group from plugin](actions/delete-gw-plugins-plugin-selector-groups-plugin-groups-selector.md) | DELETE |  |
| [List available plugins](actions/get-gw-plugins-plugin-selector.md) | GET |  |
| [Retrieve devices in plugin](actions/get-gw-plugins-plugin-selector-devices-plugin-devices-selector.md) | GET |  |
| [Retrieve geofences in plugin](actions/get-gw-plugins-plugin-selector-geofences-plugin-geofences-selector.md) | GET |  |
| [Fetch groups assigned to the plugin](actions/get-gw-plugins-plugin-selector-groups-plugin-groups-selector.md) | GET |  |
| [Retrieve plugin logs](actions/get-gw-plugins-plugin-selector-logs.md) | GET |  |
| [Retrieve raw traffic generated by plugin](actions/get-gw-plugins-plugin-selector-packets.md) | GET |  |
| [Modify plugin properties](actions/update-gw-plugins-plugin-selector.md) | PUT |  |
| [Modify full device data for plugin](actions/update-gw-plugins-plugin-selector-devices-plugin-devices-selector.md) | PUT |  |
| [Modify subset of device data for plugin](actions/update-gw-plugins-plugin-selector-devices-plugin-devices-selector2.md) | PUT |  |
| [Modify geofence data for plugin](actions/update-gw-plugins-plugin-selector-geofences-plugin-geofences-selector.md) | PUT |  |
| [Update assignment of group of devices to plugin](actions/update-gw-plugins-plugin-selector-groups-plugin-groups-selector.md) | PUT |  |
| [Modify fields inside plugin configuration](actions/update-gw-plugins-plugin-selector2.md) | PUT |  |

### Realms

| Action | Method | Description |
| --- | --- | --- |
| [Create realm](actions/create-platform-realms.md) | POST |  |
| [Bind Identity Provider to the realm](actions/create-platform-realms-realm-selector-identity-providers-realm-identity-provider-selector.md) | POST |  |
| [Calculate intervals from realm logs](actions/create-platform-realms-realm-selector-logs-calculate.md) | POST |  |
| [Create new role](actions/create-platform-realms-realm-selector-roles.md) | POST |  |
| [Create new realm user](actions/create-platform-realms-realm-selector-users.md) | POST |  |
| [Log in as user](actions/create-platform-realms-realm-selector-users-user-selector-login.md) | POST |  |
| [Log out user](actions/create-platform-realms-realm-selector-users-user-selector-logout.md) | POST |  |
| [Delete realm](actions/delete-platform-realms-realm-selector.md) | DELETE |  |
| [Remove binding of Identity Provider from realms](actions/delete-platform-realms-realm-selector-identity-providers-realm-identity-provider-selector.md) | DELETE |  |
| [Delete realm roles](actions/delete-platform-realms-realm-selector-roles-role-selector.md) | DELETE |  |
| [Delete realm users](actions/delete-platform-realms-realm-selector-users-user-selector.md) | DELETE |  |
| [Unlink identity provider accounts from user](actions/delete-platform-realms-realm-selector-users-user-selector-identity-providers-user-identity-provider-selector.md) | DELETE |  |
| [Reset user's password](actions/delete-platform-realms-realm-selector-users-user-selector-password.md) | DELETE |  |
| [Retrieve realm](actions/get-platform-realms-realm-selector.md) | GET |  |
| [Retrieve Identity Providers binded to realms](actions/get-platform-realms-realm-selector-identity-providers-realm-identity-provider-selector.md) | GET |  |
| [Retrieve realm logs](actions/get-platform-realms-realm-selector-logs.md) | GET |  |
| [Retrieve realm roles](actions/get-platform-realms-realm-selector-roles-role-selector.md) | GET |  |
| [Retrieve realm users](actions/get-platform-realms-realm-selector-users-user-selector.md) | GET |  |
| [Retrieve user confirmation code](actions/get-platform-realms-realm-selector-users-user-selector-confirmation-password.md) | GET |  |
| [Get linked identity provider accounts to user](actions/get-platform-realms-realm-selector-users-user-selector-identity-providers-user-identity-provider-selector.md) | GET |  |
| [Get confirmation link for third-party Identity Provider account binding](actions/get-platform-realms-realm-selector-users-user-selector-identity-providers-user-identity-provider-selector-confirmation.md) | GET |  |
| [Update realm configuration](actions/update-platform-realms-realm-selector.md) | PUT |  |
| [Modify the binding of Identity Provider to realms](actions/update-platform-realms-realm-selector-identity-providers-realm-identity-provider-selector.md) | PUT |  |
| [Modify realm role](actions/update-platform-realms-realm-selector-roles-role-selector.md) | PUT |  |
| [Modify realm role](actions/update-platform-realms-realm-selector-roles-role-selector2.md) | PUT |  |
| [Modify realm user](actions/update-platform-realms-realm-selector-users-user-selector.md) | PUT |  |
| [Modify realm user](actions/update-platform-realms-realm-selector-users-user-selector2.md) | PUT |  |
| [Patch item properties](actions/update-platform-realms-realm-selector2.md) | PUT |  |

### Regions

| Action | Method | Description |
| --- | --- | --- |
| [Fetch available flespi regions](actions/get-auth-regions.md) | GET |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create persistent MQTT session](actions/create-mqtt-sessions.md) | POST |  |
| [Subscribe MQTT session to a topic](actions/create-mqtt-sessions-sessions-selector-subscriptions.md) | POST |  |
| [Delete MQTT session](actions/delete-mqtt-sessions-sessions-selector.md) | DELETE |  |
| [Unsubscribe MQTT session from topic](actions/delete-mqtt-sessions-sessions-selector-subscriptions-subscriptions-selector.md) | DELETE |  |
| [Retrieve MQTT sessions](actions/get-mqtt-sessions-sessions-selector.md) | GET |  |
| [Retrieve MQTT session subscriptions](actions/get-mqtt-sessions-sessions-selector-subscriptions-subscriptions-selector.md) | GET |  |

### Stream

| Action | Method | Description |
| --- | --- | --- |
| [List streams](actions/list-streams.md) | GET |  |

### Stream Log

| Action | Method | Description |
| --- | --- | --- |
| [List stream logs](actions/list-stream-logs.md) | GET |  |

### Stream Protocols

| Action | Method | Description |
| --- | --- | --- |
| [Fetch available stream protocols](actions/get-gw-stream-protocols-stream-protocols-selector.md) | GET |  |

### Streams

| Action | Method | Description |
| --- | --- | --- |
| [Create new stream](actions/create-gw-streams.md) | POST |  |
| [Subscribe stream to channel messages](actions/create-gw-streams-stream-selector-channels-stream-channels-selector.md) | POST |  |
| [Subscribe stream to device messages](actions/create-gw-streams-stream-selector-devices-stream-devices-selector.md) | POST |  |
| [Assign geofences to stream](actions/create-gw-streams-stream-selector-geofences-stream-geofences-selector.md) | POST |  |
| [Subscribe stream to group of devices](actions/create-gw-streams-stream-selector-groups-stream-groups-selector.md) | POST |  |
| [Calculate intervals from stream logs](actions/create-gw-streams-stream-selector-logs-calculate.md) | POST |  |
| [Post messages to stream queue](actions/create-gw-streams-stream-selector-messages.md) | POST |  |
| [Delete selected streams](actions/delete-gw-streams-stream-selector.md) | DELETE |  |
| [Unsubscribe stream from channels](actions/delete-gw-streams-stream-selector-channels-stream-channels-selector.md) | DELETE |  |
| [Unsubscribe stream from devices](actions/delete-gw-streams-stream-selector-devices-stream-devices-selector.md) | DELETE |  |
| [Unassign geofences from stream](actions/delete-gw-streams-stream-selector-geofences-stream-geofences-selector.md) | DELETE |  |
| [Unsubscribe stream from group](actions/delete-gw-streams-stream-selector-groups-stream-groups-selector.md) | DELETE |  |
| [Remove all messages from the stream queue.](actions/delete-gw-streams-stream-selector-messages.md) | DELETE |  |
| [List available streams](actions/get-gw-streams-stream-selector.md) | GET |  |
| [List channels to which stream is subscribed](actions/get-gw-streams-stream-selector-channels-stream-channels-selector.md) | GET |  |
| [List devices to which stream is subscribed](actions/get-gw-streams-stream-selector-devices-stream-devices-selector.md) | GET |  |
| [Retrieve geofences in stream](actions/get-gw-streams-stream-selector-geofences-stream-geofences-selector.md) | GET |  |
| [List groups to which stream is subscribed](actions/get-gw-streams-stream-selector-groups-stream-groups-selector.md) | GET |  |
| [Retrieve stream logs](actions/get-gw-streams-stream-selector-logs.md) | GET |  |
| [Retrieve raw traffic generated by stream](actions/get-gw-streams-stream-selector-packets.md) | GET |  |
| [Modify stream properties](actions/update-gw-streams-stream-selector.md) | PUT |  |
| [Modify device data for stream](actions/update-gw-streams-stream-selector-devices-stream-devices-selector.md) | PUT |  |
| [Modify geofence data for stream](actions/update-gw-streams-stream-selector-geofences-stream-geofences-selector.md) | PUT |  |
| [Patch item properties](actions/update-gw-streams-stream-selector2.md) | PUT |  |

### Subaccounts

| Action | Method | Description |
| --- | --- | --- |
| [Create subaccount](actions/create-platform-subaccounts.md) | POST |  |
| [Calculate intervals from subaccount logs](actions/create-platform-subaccounts-subaccounts-selector-logs-calculate.md) | POST |  |
| [Delete subaccount](actions/delete-platform-subaccounts-subaccounts-selector.md) | DELETE |  |
| [Retrieve subaccounts](actions/get-platform-subaccounts-subaccounts-selector.md) | GET |  |
| [Get subaccount log records.](actions/get-platform-subaccounts-subaccounts-selector-logs.md) | GET |  |
| [Update subaccount configuration](actions/update-platform-subaccounts-subaccounts-selector.md) | PUT |  |
| [Patch item properties](actions/update-platform-subaccounts-subaccounts-selector2.md) | PUT |  |

### Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create token](actions/create-platform-tokens.md) | POST |  |
| [Calculate intervals from token logs](actions/create-platform-tokens-tokens-selector-logs-calculate.md) | POST |  |
| [Delete token](actions/delete-platform-tokens-tokens-selector.md) | DELETE |  |
| [Retrieve tokens](actions/get-platform-tokens-tokens-selector.md) | GET |  |
| [Retrieve token logs](actions/get-platform-tokens-tokens-selector-logs.md) | GET |  |
| [Update token configuration](actions/update-platform-tokens-tokens-selector.md) | PUT |  |
| [Patch item properties](actions/update-platform-tokens-tokens-selector2.md) | PUT |  |

### Tools

| Action | Method | Description |
| --- | --- | --- |
| [Consult flespi account expert](actions/create-ai-tools-consult-flespi-account.md) | POST |  |
| [Generate flespi expression](actions/create-ai-tools-generate-flespi-expression.md) | POST |  |
| [Generate PVM code](actions/create-ai-tools-generate-pvm-code.md) | POST |  |
| [Retrieve REST API method schema](actions/create-ai-tools-get-api-schema.md) | POST |  |
| [Search for REST API methods](actions/create-ai-tools-search-api-methods.md) | POST |  |
| [Search device documentation](actions/create-ai-tools-search-device-documentation.md) | POST |  |
| [Search flespi platform documentation](actions/create-ai-tools-search-flespi-documentation.md) | POST |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve realm user information](actions/get-realm-realm-public-id-user.md) | GET |  |
| [Set realm user password](actions/update-realm-realm-public-id-user.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List webhooks](actions/list-webhooks.md) | GET |  |

### Webhooks

| Action | Method | Description |
| --- | --- | --- |
| [Create webhook](actions/create-platform-webhooks.md) | POST |  |
| [Calculate intervals from webhook logs](actions/create-platform-webhooks-webhooks-selector-logs-calculate.md) | POST |  |
| [Delete webhook](actions/delete-platform-webhooks-webhooks-selector.md) | DELETE |  |
| [Retrieve webhooks](actions/get-platform-webhooks-webhooks-selector.md) | GET |  |
| [Retrieve webhook logs](actions/get-platform-webhooks-webhooks-selector-logs.md) | GET |  |
| [Retrieve raw traffic of actions performed by webhook](actions/get-platform-webhooks-webhooks-selector-packets.md) | GET |  |
| [Update webhook configuration](actions/update-platform-webhooks-webhooks-selector.md) | PUT |  |
| [Patch item properties](actions/update-platform-webhooks-webhooks-selector2.md) | PUT |  |

