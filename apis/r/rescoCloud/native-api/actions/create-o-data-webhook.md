# Create OData Webhook with Resco Cloud

Creates an OData webhook in Resco Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `https://{organization}.rescocrm.com/odata/v4/$hook`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [Create OData Webhook](https://docs.resco.net/wiki/OData_service)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$entity` | query | `string` | yes | Entity name for the webhook subscription. |
| `$action` | query | `string` | yes | Webhook action: Create, Update, or Delete. |
| `rawBody` | body | `string` | yes | JSON webhook body. Example: {"Url":{"CallbackUrl":"https://example.com/webhook"}}. |
