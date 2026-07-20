# Edit instant email with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/instant-emails/{emailId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Edit instant email](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | yes | ID of the instant email to edit |
| `from` | body | `string` | yes | — |
| `to` | body | `string` | yes | — |
| `subject` | body | `string` | yes | — |
| `body` | body | `string` | no | — |
| `status` | body | `string` | no | — |
| `typeOfMail` | body | `string` | yes | — |
| `selectTemplate` | body | `boolean` | no | — |
