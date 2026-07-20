# Add an email to a campaign with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/campaigns/{campaignId}/addmail`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Add an email to a campaign](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | ID of the campaign to add an email to |
| `subject` | body | `string` | no | — |
| `body` | body | `string` | no | — |
| `typeOfMail` | body | `string` | no | — |
| `emailInterval` | body | `number` | no | — |
| `selectTemplate` | body | `boolean` | no | — |
