# Update Webhook with IndyForms

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/public/v2/webhooks`
- **Base URL:** `https://api.indyforms.com`
- **Official documentation:** [Update Webhook](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | query | `string` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `endpointAddress` | body | `string` | no |
| `raisedFor[]` | body | `array<string>` | no |
| `isActive` | body | `boolean` | no |
