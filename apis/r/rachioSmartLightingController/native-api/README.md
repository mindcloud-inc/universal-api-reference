# Rachio Smart Lighting Controller: Native API Reference

A consolidated summary of Rachio Smart Lighting Controller's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://rachio.readme.io/reference/getting-started
- **API base URL:** `https://cloud-rest.rach.io`

## Authentication

### API Key

Authenticate with a Rachio API key copied from Account Settings.

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
| [Activate Lighting Scene](actions/activate-lighting-scene.md) | `PUT https://cloud-rest.rach.io/lighting/activateLightingScene/:id` | [docs](https://rachio.readme.io/reference/lightingservice_activatelightingscene) |
| [Create Lighting Program](actions/create-lighting-program.md) | `POST https://cloud-rest.rach.io/lighting/createLightingProgram` | [docs](https://rachio.readme.io/reference/lightingservice_createlightingprogram) |
| [Create Lighting Scene](actions/create-lighting-scene.md) | `POST https://cloud-rest.rach.io/lighting/createLightingScene` | [docs](https://rachio.readme.io/reference/lightingservice_createlightingscene) |
| [Create Lighting Zone Group](actions/create-lighting-zone-group.md) | `POST https://cloud-rest.rach.io/lighting/createLightingZoneGroup` | [docs](https://rachio.readme.io/reference/lightingservice_createlightingzonegroup) |
| [Create Webhook](actions/create-webhook.md) | `POST https://cloud-rest.rach.io/webhook/createWebhook` | [docs](https://rachio.readme.io/reference/webhookservice_createwebhook) |
| [Deactivate Lighting Scene](actions/deactivate-lighting-scene.md) | `PUT https://cloud-rest.rach.io/lighting/deactivateLightingScene/:id` | [docs](https://rachio.readme.io/reference/lightingservice_deactivatelightingscene) |
| [Delete All Webhooks](actions/delete-all-webhooks.md) | `DELETE https://cloud-rest.rach.io/webhook/deleteAllWebhooks` | [docs](https://rachio.readme.io/reference/webhookservice_deleteallwebhooks) |
| [Delete Lighting Program](actions/delete-lighting-program.md) | `DELETE https://cloud-rest.rach.io/lighting/deleteLightingProgram/:id` | [docs](https://rachio.readme.io/reference/lightingservice_deletelightingprogram) |
| [Delete Lighting Scene](actions/delete-lighting-scene.md) | `DELETE https://cloud-rest.rach.io/lighting/deleteLightingScene/:id` | [docs](https://rachio.readme.io/reference/lightingservice_deletelightingscene) |
| [Delete Lighting Zone Group](actions/delete-lighting-zone-group.md) | `DELETE https://cloud-rest.rach.io/lighting/deleteLightingZoneGroup/:id` | [docs](https://rachio.readme.io/reference/lightingservice_deletelightingzonegroup) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE https://cloud-rest.rach.io/webhook/deleteWebhook/:id` | [docs](https://rachio.readme.io/reference/webhookservice_deletewebhook) |
| [Get Current Person Details](actions/get-current-person-details.md) | `GET https://api.rach.io/1/public/person/:id` | [docs](https://rachio.readme.io/reference/publicpersonid) |
| [Get Current Person ID](actions/get-current-person-id.md) | `GET https://api.rach.io/1/public/person/info` | [docs](https://rachio.readme.io/reference/publicpersoninfo) |
| [List Lighting Areas](actions/list-lighting-areas.md) | `GET https://cloud-rest.rach.io/lighting/listLightingAreas/:userId` | [docs](https://rachio.readme.io/reference/lightingservice_listlightingareas) |
| [List Lighting Programs](actions/list-lighting-programs.md) | `GET https://cloud-rest.rach.io/lighting/listLightingPrograms` | [docs](https://rachio.readme.io/reference/lightingservice_listlightingprograms) |
| [List Lighting Zones](actions/list-lighting-zones.md) | `GET https://cloud-rest.rach.io/lighting/listLightingZones` | [docs](https://rachio.readme.io/reference/lightingservice_listlightingzones) |
| [List Properties](actions/list-properties.md) | `GET https://cloud-rest.rach.io/property/listProperties/:userId` | [docs](https://rachio.readme.io/reference/propertyservice_listproperties) |
| [List Webhook Event Types](actions/list-webhook-event-types.md) | `GET https://cloud-rest.rach.io/webhook/listWebhookEventTypes` | [docs](https://rachio.readme.io/reference/webhookservice_listwebhookeventtypes) |
| [List Webhooks](actions/list-webhooks.md) | `GET https://cloud-rest.rach.io/webhook/listWebhooks` | [docs](https://rachio.readme.io/reference/webhookservice_listwebhooks) |
| [Set Lighting Zone Desired Dimming Settings](actions/set-lighting-zone-desired-dimming-settings.md) | `PUT https://cloud-rest.rach.io/lighting/setLightingZoneDesiredDimmingSettings` | [docs](https://rachio.readme.io/reference/lightingservice_setlightingzonedesireddimmingsettings) |
| [Set Lighting Zone Dimming Levels](actions/set-lighting-zone-dimming-levels.md) | `PUT https://cloud-rest.rach.io/lighting/setLightingZoneDimmingLevels` | [docs](https://rachio.readme.io/reference/lightingservice_setlightingzonedimminglevels) |
| [Set Lighting Zone States](actions/set-lighting-zone-states.md) | `PUT https://cloud-rest.rach.io/lighting/setLightingZoneStates` | [docs](https://rachio.readme.io/reference/lightingservice_setlightingzonestates) |
| [Update Lighting Controller](actions/update-lighting-controller.md) | `PUT https://cloud-rest.rach.io/lighting/updateLightingController` | [docs](https://rachio.readme.io/reference/lightingservice_updatelightingcontroller) |
| [Update Lighting Program](actions/update-lighting-program.md) | `PUT https://cloud-rest.rach.io/lighting/updateLightingProgram` | [docs](https://rachio.readme.io/reference/lightingservice_updatelightingprogram) |
| [Update Lighting Scene](actions/update-lighting-scene.md) | `PUT https://cloud-rest.rach.io/lighting/updateLightingScene` | [docs](https://rachio.readme.io/reference/lightingservice_updatelightingscene) |
| [Update Lighting Zone](actions/update-lighting-zone.md) | `PUT https://cloud-rest.rach.io/lighting/updateLightingZone` | [docs](https://rachio.readme.io/reference/lightingservice_updatelightingzone) |
| [Update Lighting Zone Group](actions/update-lighting-zone-group.md) | `PUT https://cloud-rest.rach.io/lighting/updateLightingZoneGroup` | [docs](https://rachio.readme.io/reference/lightingservice_updatelightingzonegroup) |
| [Update Webhook](actions/update-webhook.md) | `PUT https://cloud-rest.rach.io/webhook/updateWebhook` | [docs](https://rachio.readme.io/reference/webhookservice_updatewebhook) |
