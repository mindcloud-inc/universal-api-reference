# <img src="https://images.mindcloud.co/apps/icons/we-be-home_1776363887662.png" alt="WeBeHome logo" width="28" height="28"> WeBeHome: Universal API

WeBeHome is a smart home and security platform for monitoring locations, devices, automations, users, alerts, and gateway status across connected homes or buildings.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/weBeHome/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 88
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.webehome.com/en
- **Vendor API docs:** https://www.webehome.com/en/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Customer Configuration](actions/get-customer-configuration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/get-customer-configuration?connectionId=$CONNECTION_ID&HtmlTable=no&Heading=Yes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (88)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create Device Token](actions/create-device-token.md) | POST |  |
| [Delete Web Token](actions/delete-web-token.md) | DELETE |  |
| [Login Account User](actions/login-account-user.md) | POST |  |
| [Logout User Token](actions/logout-user-token.md) | DELETE |  |

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Get Action Set Auto Sun Device List](actions/get-action-set-auto-sun-device-list.md) | GET |  |
| [Get Action Set Device List](actions/get-action-set-device-list.md) | GET |  |
| [Get Action Set Light Sensor Device List](actions/get-action-set-light-sensor-device-list.md) | GET |  |
| [Get Action Set Thermostat Device List](actions/get-action-set-thermostat-device-list.md) | GET |  |
| [Get Heating Zone Related Door Windows](actions/get-heating-zone-related-door-windows.md) | GET |  |
| [List Action Sets](actions/list-action-sets.md) | GET |  |
| [Load Action](actions/load-action.md) | GET |  |
| [Load Action Set](actions/load-action-set.md) | GET |  |
| [Remove Action](actions/remove-action.md) | DELETE |  |
| [Remove Action Set](actions/remove-action-set.md) | DELETE |  |
| [Save Action](actions/save-action.md) | PUT |  |
| [Save Action Set](actions/save-action-set.md) | PUT |  |
| [Save Action Set Show In Main](actions/save-action-set-show-in-main.md) | PUT |  |
| [Save Heating Zone Related Door Windows](actions/save-heating-zone-related-door-windows.md) | PUT |  |
| [Start Scene Action Set](actions/start-scene-action-set.md) | PUT |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create New Customer Token](actions/create-new-customer-token.md) | POST |  |
| [Get Customer Configuration](actions/get-customer-configuration.md) | GET |  |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Add Device](actions/add-device.md) | POST |  |
| [Add Device Event](actions/add-device-event.md) | POST |  |
| [Cancel Device Add](actions/cancel-device-add.md) | DELETE |  |
| [Cancel Device Remove](actions/cancel-device-remove.md) | DELETE |  |
| [Change Device Status](actions/change-device-status.md) | PUT |  |
| [Delete User Device](actions/delete-user-device.md) | DELETE |  |
| [Get Base Unit Configuration](actions/get-base-unit-configuration.md) | GET |  |
| [Get Device Status](actions/get-device-status.md) | GET |  |
| [Load Device Advanced Settings](actions/load-device-advanced-settings.md) | GET |  |
| [Remove Device](actions/remove-device.md) | DELETE |  |
| [Save Device Advanced Settings](actions/save-device-advanced-settings.md) | PUT |  |
| [Save Device Favorite](actions/save-device-favorite.md) | PUT |  |
| [Save Device Relations](actions/save-device-relations.md) | PUT |  |
| [Save Device Show In Main](actions/save-device-show-in-main.md) | PUT |  |
| [Save User Device](actions/save-user-device.md) | PUT |  |
| [Set Device Value](actions/set-device-value.md) | PUT |  |
| [Set Switch Status](actions/set-switch-status.md) | PUT |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Data](actions/get-event-data.md) | GET |  |
| [Get Reference Events](actions/get-reference-events.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Arm Location Away](actions/arm-location-away.md) | PUT |  |
| [Arm Location Home](actions/arm-location-home.md) | PUT |  |
| [Clear Location Status](actions/clear-location-status.md) | PUT |  |
| [Disarm Location](actions/disarm-location.md) | PUT |  |
| [Get Location Connection Info](actions/get-location-connection-info.md) | GET |  |
| [Get Location Device List](actions/get-location-device-list.md) | GET |  |
| [Get Location Devices](actions/get-location-devices.md) | GET |  |
| [Get Location Events](actions/get-location-events.md) | GET |  |
| [Get Location Status](actions/get-location-status.md) | GET |  |
| [Load Location](actions/load-location.md) | GET |  |
| [Pair Location Gateway](actions/pair-location-gateway.md) | PUT |  |
| [Register Location Webhook](actions/register-location-webhook.md) | POST |  |
| [Request Location Permission](actions/request-location-permission.md) | POST |  |
| [Save Location](actions/save-location.md) | PUT |  |
| [Save Location Device List](actions/save-location-device-list.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Change Group Status](actions/change-group-status.md) | PUT |  |
| [Check Login Name Availability](actions/check-login-name-availability.md) | GET |  |
| [Get Add Device Documentation Content](actions/get-add-device-documentation-content.md) | GET |  |
| [Get Add Device Documentation List](actions/get-add-device-documentation-list.md) | GET |  |
| [Get FAQ Article](actions/get-faq-article.md) | GET |  |
| [Get FAQ Category Tree](actions/get-faq-category-tree.md) | GET |  |
| [Get Measurement Data](actions/get-measurement-data.md) | GET |  |
| [Get Remove Device Documentation Content](actions/get-remove-device-documentation-content.md) | GET |  |
| [Initialize Video Support Session](actions/initialize-video-support-session.md) | POST |  |
| [List Countries](actions/list-countries.md) | GET |  |
| [List Geo Names](actions/list-geo-names.md) | GET |  |
| [List Groups](actions/list-groups.md) | GET |  |
| [List Time Zones](actions/list-time-zones.md) | GET |  |
| [Load Group](actions/load-group.md) | GET |  |
| [Load Terms Of Service](actions/load-terms-of-service.md) | GET |  |
| [Poll Video Support For Other Part](actions/poll-video-support-for-other-part.md) | GET |  |
| [Save Group](actions/save-group.md) | PUT |  |
| [Send Contact Request](actions/send-contact-request.md) | POST |  |
| [Track Analytics Event](actions/track-analytics-event.md) | POST |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Accept User Terms Of Service](actions/accept-user-terms-of-service.md) | PUT |  |
| [Change User Email And Password](actions/change-user-email-and-password.md) | PUT |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Dismiss User Message](actions/dismiss-user-message.md) | PUT |  |
| [Get User Messages](actions/get-user-messages.md) | GET |  |
| [Get User Notification List](actions/get-user-notification-list.md) | GET |  |
| [Get User Roles](actions/get-user-roles.md) | GET |  |
| [Invite User](actions/invite-user.md) | POST |  |
| [List Users](actions/list-users-for-location.md) | GET |  |
| [Load User](actions/load-user.md) | GET |  |
| [Load User Terms Of Service](actions/load-user-terms-of-service.md) | GET |  |
| [Revoke User Access](actions/revoke-user-access.md) | DELETE |  |
| [Save User](actions/save-user.md) | PUT |  |
| [Set User Notification](actions/set-user-notification.md) | PUT |  |

