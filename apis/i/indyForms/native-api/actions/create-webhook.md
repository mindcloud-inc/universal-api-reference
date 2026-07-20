# Create Webhook with IndyForms

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/v2/webhooks`
- **Base URL:** `https://api.indyforms.com`
- **Official documentation:** [Create Webhook](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `endpointAddress` | body | `string` | no |
| `raisedFor[]` | body | `array<string>` | no |
| `isActive` | body | `boolean` | no |
