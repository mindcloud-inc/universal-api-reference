# Rachio Smart Hose Timer: Native API Reference

A consolidated summary of Rachio Smart Hose Timer's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://rachio.readme.io/reference/getting-started
- **API base URL:** `https://api.rach.io/1`

## Authentication

### API Key

Connect with a Rachio API key copied from the Rachio account profile.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://rachio.readme.io/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Notification Webhook](actions/create-notification-webhook.md) | `POST /public/notification/webhook` | [docs](https://rachio.readme.io/reference/publicnotificationwebhook) |
| [Create Planned Run Skip Overrides](actions/create-planned-run-skip-overrides.md) | `POST https://cloud-rest.rach.io/program/createPlannedRunSkipOverrides` | [docs](https://rachio.readme.io/reference/programservice_createplannedrunskipoverrides) |
| [Create Program V2](actions/create-program-v2.md) | `POST https://cloud-rest.rach.io/program/createProgramV2` | [docs](https://rachio.readme.io/reference/programservice_createprogramv2) |
| [Create Skip Overrides](actions/create-skip-overrides.md) | `POST https://cloud-rest.rach.io/program/createSkipOverrides` | [docs](https://rachio.readme.io/reference/programservice_createskipoverrides) |
| [Create Webhook](actions/create-webhook.md) | `POST https://cloud-rest.rach.io/webhook/createWebhook` | [docs](https://rachio.readme.io/reference/webhookservice_createwebhook) |
| [Delete Notification Webhook](actions/delete-notification-webhook.md) | `DELETE /public/notification/webhook/:id` | [docs](https://rachio.readme.io/reference/publicnotificationwebhookid) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE https://cloud-rest.rach.io/webhook/deleteWebhook/:id` | [docs](https://rachio.readme.io/reference/webhookservice_deletewebhook) |
| [Find Property By Entity](actions/find-property-by-entity.md) | `GET https://cloud-rest.rach.io/property/findPropertyByEntity` | [docs](https://rachio.readme.io/reference/propertyservice_findpropertybyentity) |
| [Get Controller Device](actions/get-controller-device.md) | `GET /public/device/:id` | [docs](https://rachio.readme.io/reference/publicdeviceid) |
| [Get Current Person Info](actions/get-current-person-info.md) | `GET /public/person/info` | [docs](https://rachio.readme.io/reference/publicpersoninfo) |
| [Get Current Schedule](actions/get-current-schedule.md) | `GET /public/device/:id/current_schedule` | [docs](https://rachio.readme.io/reference/publicdeviceidcurrent_schedule) |
| [Get Device Forecast](actions/get-device-forecast.md) | `GET /public/device/:id/forecast` | [docs](https://rachio.readme.io/reference/publicdeviceidforecastunitsunits) |
| [Get Notification Webhook](actions/get-notification-webhook.md) | `GET /public/notification/webhook/:id` | [docs](https://rachio.readme.io/reference/publicnotificationwebhookid-1) |
| [Get Person](actions/get-person.md) | `GET /public/person/:id` | [docs](https://rachio.readme.io/reference/publicpersonid) |
| [Get Property](actions/get-property.md) | `GET https://cloud-rest.rach.io/property/getProperty/:id` | [docs](https://rachio.readme.io/reference/propertyservice_getproperty) |
| [Get Valve Day Views](actions/get-valve-day-views.md) | `POST https://cloud-rest.rach.io/summary/getValveDayViews` | [docs](https://rachio.readme.io/reference/summaryservice_getvalvedayviews) |
| [Get Webhook](actions/get-webhook.md) | `GET https://cloud-rest.rach.io/webhook/getWebhook/:id` | [docs](https://rachio.readme.io/reference/webhookservice_getwebhook) |
| [List Base Stations](actions/list-base-stations.md) | `GET https://cloud-rest.rach.io/valve/listBaseStations/:userId` | [docs](https://rachio.readme.io/reference/valveservice_listbasestations) |
| [List Device Events](actions/list-device-events.md) | `GET /public/device/:id/event` | [docs](https://rachio.readme.io/reference/publicdeviceideventstarttimestarttimeendtimeendtim) |
| [List Device Webhooks](actions/list-device-webhooks.md) | `GET /public/notification/:deviceId/webhook` | [docs](https://rachio.readme.io/reference/publicnotificationdeviceidwebhook) |
| [List Notification Webhook Event Types](actions/list-notification-webhook-event-types.md) | `GET /public/notification/webhook_event_type` | [docs](https://rachio.readme.io/reference/publicnotificationwebhook_event_type) |
| [List Programs V2](actions/list-programs-v2.md) | `GET https://cloud-rest.rach.io/program/listProgramsV2` | [docs](https://rachio.readme.io/reference/programservice_listprogramsv2) |
| [List Properties](actions/list-properties.md) | `GET https://cloud-rest.rach.io/property/listProperties/:userId` | [docs](https://rachio.readme.io/reference/propertyservice_listproperties) |
| [List Webhook Event Types](actions/list-webhook-event-types.md) | `GET https://cloud-rest.rach.io/webhook/listWebhookEventTypes` | [docs](https://rachio.readme.io/reference/webhookservice_listwebhookeventtypes) |
| [List Webhooks](actions/list-webhooks.md) | `GET https://cloud-rest.rach.io/webhook/listWebhooks` | [docs](https://rachio.readme.io/reference/webhookservice_listwebhooks) |
| [Update Notification Webhook](actions/update-notification-webhook.md) | `PUT /public/notification/webhook` | [docs](https://rachio.readme.io/reference/publicnotificationwebhook-1) |
| [Update Program V2](actions/update-program-v2.md) | `PUT https://cloud-rest.rach.io/program/updateProgramV2` | [docs](https://rachio.readme.io/reference/programservice_updateprogramv2) |
| [Update Webhook](actions/update-webhook.md) | `PUT https://cloud-rest.rach.io/webhook/updateWebhook` | [docs](https://rachio.readme.io/reference/webhookservice_updatewebhook) |
