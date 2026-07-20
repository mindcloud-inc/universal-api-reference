# Create Webhook with Fillout Forms

Creates a webhook in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/create`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Create Webhook](https://www.fillout.com/help/api-reference/create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | body | `string` | yes | The form ID to subscribe to. |
| `url` | body | `string` | yes | The webhook destination URL. |
