# Create Development App From Production App with Tabidoo

Creates a development app from a production app in Tabidoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/createDevAppFromProdApp`
- **Base URL:** `https://app.tabidoo.cloud/api/v2`
- **Official documentation:** [Create Development App From Production App](https://help.tabidoo.cloud/en/article/creating-a-development-app-from-a-production-app)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicationId` | body | `string` | yes | The production Tabidoo application ID to clone into a DEV app. |
| `overrideExistingTemplateId` | body | `string` | no | Optional template ID required when the production app was already linked to a previous DEV template and you want to force creating a new DEV app. |
