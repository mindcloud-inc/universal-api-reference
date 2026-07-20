# Create Webhook with Recommand

Creates a new webhook in Recommand.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhooks`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Create Webhook](https://recommand.eu/en/reference/webhooks/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `string` | no | companyId body field. |
| `url` | body | `string` | yes | url body field. |
