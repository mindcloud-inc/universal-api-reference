# WeBeHome: Native API Reference

A consolidated summary of WeBeHome's API configuration and 88 documented operations, with links to official documentation.

- **Official docs:** https://www.webehome.com/en/docs
- **OpenAPI specification:** https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf
- **API base URL:** `https://webehome.com/API`

## Authentication

### WeBeHome Credentials

Use WeBeHome login credentials for Customer API actions and a freshly created JWT for Open API actions.

### Credentials

- **Login Name:** `loginName` · required · WeBeHome account login name or email used for Customer API calls and JWT creation.
- **Password:** `password` · required · WeBeHome account password used for Customer API calls and JWT creation.
- **JWT:** `jwt` · required · User JWT created from CreateWebTokens/LoginAccountUser and used as the bearer token for Open API calls.

Send these headers with each API request:

```http
Authorization: Bearer <jwt>
```

[Official authentication documentation](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf)

## Endpoints (88 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept User Terms Of Service](actions/accept-user-terms-of-service.md) | `POST OpenAPIservice.svc/User/AcceptTermsOfService` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Add Device](actions/add-device.md) | `POST OpenAPIservice.svc/Device/Add` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Add Device Event](actions/add-device-event.md) | `POST OpenAPIservice.svc/Device/AddEvent` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Arm Location Away](actions/arm-location-away.md) | `POST OpenAPIservice.svc/Location/ArmAway` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Arm Location Home](actions/arm-location-home.md) | `POST OpenAPIservice.svc/Location/ArmHome` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Cancel Device Add](actions/cancel-device-add.md) | `POST OpenAPIservice.svc/Device/AddCancel` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Cancel Device Remove](actions/cancel-device-remove.md) | `POST OpenAPIservice.svc/Device/RemoveCancel` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Change Device Status](actions/change-device-status.md) | `POST OpenAPIservice.svc/Device/ChangeStatus` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Change Group Status](actions/change-group-status.md) | `POST OpenAPIservice.svc/Group/ChangeStatus` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Change User Email And Password](actions/change-user-email-and-password.md) | `POST OpenAPIservice.svc/User/ChangeEmailAndPassword` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Check Login Name Availability](actions/check-login-name-availability.md) | `POST OpenAPIservice.svc/CreateWebTokens/CheckLoginName` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Clear Location Status](actions/clear-location-status.md) | `POST OpenAPIservice.svc/Location/Clear` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Create Device Token](actions/create-device-token.md) | `POST OpenAPIservice.svc/CreateWebTokens/CreateDevice` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Create New Customer Token](actions/create-new-customer-token.md) | `POST OpenAPIservice.svc/CreateWebTokens/NewCustomer` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Delete User](actions/delete-user.md) | `POST OpenAPIservice.svc/User/Delete` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Delete User Device](actions/delete-user-device.md) | `POST OpenAPIservice.svc/UserDevice/Delete` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Delete Web Token](actions/delete-web-token.md) | `POST OpenAPIservice.svc/CreateWebTokens/Delete` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Disarm Location](actions/disarm-location.md) | `POST OpenAPIservice.svc/Location/Disarm` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Dismiss User Message](actions/dismiss-user-message.md) | `POST OpenAPIservice.svc/User/MessageDismiss` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Action Set Auto Sun Device List](actions/get-action-set-auto-sun-device-list.md) | `POST OpenAPIservice.svc/ActionSet/GetDeviceListAutosun` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Action Set Device List](actions/get-action-set-device-list.md) | `POST OpenAPIservice.svc/ActionSet/GetDeviceList` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Action Set Light Sensor Device List](actions/get-action-set-light-sensor-device-list.md) | `POST OpenAPIservice.svc/ActionSet/GetDeviceListLightSensor` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Action Set Thermostat Device List](actions/get-action-set-thermostat-device-list.md) | `POST OpenAPIservice.svc/ActionSet/GetDeviceListThermostat` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Add Device Documentation Content](actions/get-add-device-documentation-content.md) | `POST OpenAPIservice.svc/Doc/GetAddContent` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Add Device Documentation List](actions/get-add-device-documentation-list.md) | `POST OpenAPIservice.svc/Doc/GetAddDeviceList` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Base Unit Configuration](actions/get-base-unit-configuration.md) | `GET WebAPI.aspx` | [docs](https://www.webehome.com/Doc/WBH_Customer_API.pdf) |
| [Get Customer Configuration](actions/get-customer-configuration.md) | `GET WebAPI.aspx` | [docs](https://www.webehome.com/Doc/WBH_Customer_API.pdf) |
| [Get Device Status](actions/get-device-status.md) | `GET WebAPI.aspx` | [docs](https://www.webehome.com/Doc/WBH_Customer_API.pdf) |
| [Get Event Data](actions/get-event-data.md) | `GET WebAPI.aspx` | [docs](https://www.webehome.com/Doc/WBH_Customer_API.pdf) |
| [Get FAQ Article](actions/get-faq-article.md) | `POST OpenAPIservice.svc/FAQ/GetArticle` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get FAQ Category Tree](actions/get-faq-category-tree.md) | `POST OpenAPIservice.svc/FAQ/GetCategoryTree` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Heating Zone Related Door Windows](actions/get-heating-zone-related-door-windows.md) | `POST OpenAPIservice.svc/ActionSet/GetHeatingZoneRelatedDoorWindows` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Location Connection Info](actions/get-location-connection-info.md) | `POST OpenAPIservice.svc/Location/ConnectionInfo` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Location Device List](actions/get-location-device-list.md) | `POST OpenAPIservice.svc/Location/GetDeviceList2` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Location Devices](actions/get-location-devices.md) | `POST OpenAPIservice.svc/Location/GetDevices` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Location Events](actions/get-location-events.md) | `POST OpenAPIservice.svc/Location/GetEvents` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Location Status](actions/get-location-status.md) | `POST OpenAPIservice.svc/Location/GetStatus3` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get Measurement Data](actions/get-measurement-data.md) | `GET WebAPI.aspx` | [docs](https://www.webehome.com/Doc/WBH_Customer_API.pdf) |
| [Get Reference Events](actions/get-reference-events.md) | `GET WebAPI.aspx` | [docs](https://www.webehome.com/Doc/WBH_Customer_API.pdf) |
| [Get Remove Device Documentation Content](actions/get-remove-device-documentation-content.md) | `POST OpenAPIservice.svc/Doc/GetRemoveContent` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get User Messages](actions/get-user-messages.md) | `POST OpenAPIservice.svc/User/Messages` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get User Notification List](actions/get-user-notification-list.md) | `POST OpenAPIservice.svc/User/GetNotificationList` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Get User Roles](actions/get-user-roles.md) | `POST OpenAPIservice.svc/User/GetRoles` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Initialize Video Support Session](actions/initialize-video-support-session.md) | `POST OpenAPIservice.svc/VideoSupport/InitSession` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Invite User](actions/invite-user.md) | `POST OpenAPIservice.svc/User/Invite` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [List Action Sets](actions/list-action-sets.md) | `POST OpenAPIservice.svc/ActionSet/List2` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [List Countries](actions/list-countries.md) | `POST OpenAPIservice.svc/Data/CountryList` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [List Geo Names](actions/list-geo-names.md) | `POST OpenAPIservice.svc/Data/GeoNameList` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [List Groups](actions/list-groups.md) | `POST OpenAPIservice.svc/Group/List` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [List Time Zones](actions/list-time-zones.md) | `POST OpenAPIservice.svc/Data/TimeZoneList` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [List Users](actions/list-users-for-location.md) | `POST OpenAPIservice.svc/User/List` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Load Action](actions/load-action.md) | `POST OpenAPIservice.svc/Action/Load` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Load Action Set](actions/load-action-set.md) | `POST OpenAPIservice.svc/ActionSet/Load2` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Load Device Advanced Settings](actions/load-device-advanced-settings.md) | `POST OpenAPIservice.svc/Device/LoadAdvanced` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Load Group](actions/load-group.md) | `POST OpenAPIservice.svc/Group/Load` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Load Location](actions/load-location.md) | `POST OpenAPIservice.svc/Location/Load` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Load Terms Of Service](actions/load-terms-of-service.md) | `POST OpenAPIservice.svc/Data/LoadTermsOfService` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Load User](actions/load-user.md) | `POST OpenAPIservice.svc/User/Load` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Load User Terms Of Service](actions/load-user-terms-of-service.md) | `POST OpenAPIservice.svc/User/LoadTermsOfService` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Login Account User](actions/login-account-user.md) | `POST OpenAPIservice.svc/CreateWebTokens/LoginAccountUser` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Logout User Token](actions/logout-user-token.md) | `POST OpenAPIservice.svc/CreateWebTokens/LogoutUser` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Pair Location Gateway](actions/pair-location-gateway.md) | `POST OpenAPIservice.svc/Location/PairGateway` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Poll Video Support For Other Part](actions/poll-video-support-for-other-part.md) | `POST OpenAPIservice.svc/VideoSupport/PollForOtherPart` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Register Location Webhook](actions/register-location-webhook.md) | `POST OpenAPIservice.svc/Location/RegisterWebHook` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Remove Action](actions/remove-action.md) | `POST OpenAPIservice.svc/Action/Remove` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Remove Action Set](actions/remove-action-set.md) | `POST OpenAPIservice.svc/ActionSet/Remove` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Remove Device](actions/remove-device.md) | `POST OpenAPIservice.svc/Device/Remove` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Request Location Permission](actions/request-location-permission.md) | `POST OpenAPIservice.svc/Location/RequestPermission` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Revoke User Access](actions/revoke-user-access.md) | `POST OpenAPIservice.svc/User/Revoke` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save Action](actions/save-action.md) | `POST OpenAPIservice.svc/Action/Save` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save Action Set](actions/save-action-set.md) | `POST OpenAPIservice.svc/ActionSet/Save2` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save Action Set Show In Main](actions/save-action-set-show-in-main.md) | `POST OpenAPIservice.svc/ActionSet/SaveShowInMain` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save Device Advanced Settings](actions/save-device-advanced-settings.md) | `POST OpenAPIservice.svc/Device/SaveAdvanced` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save Device Favorite](actions/save-device-favorite.md) | `POST OpenAPIservice.svc/Device/SaveFavorite` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save Device Relations](actions/save-device-relations.md) | `POST OpenAPIservice.svc/Device/SaveRelations` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save Device Show In Main](actions/save-device-show-in-main.md) | `POST OpenAPIservice.svc/Device/SaveShowInMain` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save Group](actions/save-group.md) | `POST OpenAPIservice.svc/Group/Save` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save Heating Zone Related Door Windows](actions/save-heating-zone-related-door-windows.md) | `POST OpenAPIservice.svc/ActionSet/SaveHeatingZoneRelatedDoorWindows` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save Location](actions/save-location.md) | `POST OpenAPIservice.svc/Location/Save` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save Location Device List](actions/save-location-device-list.md) | `POST OpenAPIservice.svc/Location/SaveDeviceList2` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save User](actions/save-user.md) | `POST OpenAPIservice.svc/User/Save` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Save User Device](actions/save-user-device.md) | `POST OpenAPIservice.svc/UserDevice/Save` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Send Contact Request](actions/send-contact-request.md) | `POST OpenAPIservice.svc/Contact/Request` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Set Device Value](actions/set-device-value.md) | `POST OpenAPIservice.svc/Device/SetValue` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Set Switch Status](actions/set-switch-status.md) | `GET WebAPI.aspx` | [docs](https://www.webehome.com/Doc/WBH_Customer_API.pdf) |
| [Set User Notification](actions/set-user-notification.md) | `POST OpenAPIservice.svc/User/SetNotification` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Start Scene Action Set](actions/start-scene-action-set.md) | `POST OpenAPIservice.svc/ActionSet/StartScene` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
| [Track Analytics Event](actions/track-analytics-event.md) | `POST OpenAPIservice.svc/Analytics/Track` | [docs](https://www.webehome.com/Doc/WeBeHomeOpenAPI.pdf) |
