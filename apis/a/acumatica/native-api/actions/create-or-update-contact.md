# Create or Update Contact with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Contact`
- **Base URL:** `{uRL}`
- **Official documentation:** [Create or Update Contact](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ContactID` | body | `object` | no | — |
| `ContactID.value` | body | `number` | no | Existing numeric Contact ID when updating; leave blank to create. |
| `FirstName` | body | `object` | no | — |
| `FirstName.value` | body | `string` | no | — |
| `LastName` | body | `object` | no | — |
| `LastName.value` | body | `string` | yes | — |
| `Email` | body | `object` | no | — |
| `Email.value` | body | `string` | no | — |
| `BusinessAccount` | body | `object` | no | — |
| `BusinessAccount.value` | body | `string` | no | — |
| `Type` | body | `object` | no | — |
| `Type.value` | body | `string` | no | — |
