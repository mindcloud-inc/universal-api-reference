# Update Webhook with Recommand

Updates an existing webhook in Recommand.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/webhooks/:webhookId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Update Webhook](https://recommand.eu/en/reference/webhooks/update-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `string` | no | companyId body field. |
| `url` | body | `string` | yes | url body field. |
| `webhookId` | path | `string` | yes | webhookId parameter. |
