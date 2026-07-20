# Create Form Webhook with Fillout

Creates a form webhook in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/create`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Create Form Webhook](https://fillout.com/help/api-reference/create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | body | `string` | yes | The public identifier of the form. |
| `url` | body | `string` | yes | The webhook destination URL. |
