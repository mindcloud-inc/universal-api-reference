# Create or Update Customer with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Customer`
- **Base URL:** `{uRL}`
- **Official documentation:** [Create or Update Customer](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerID` | body | `object` | no | — |
| `CustomerID.value` | body | `string` | yes | Unique Acumatica customer identifier. |
| `CustomerName` | body | `object` | no | — |
| `CustomerName.value` | body | `string` | yes | — |
| `CustomerClass` | body | `object` | no | — |
| `CustomerClass.value` | body | `string` | no | — |
| `Status` | body | `object` | no | — |
| `Status.value` | body | `string` | no | — |
| `AccountRef` | body | `object` | no | — |
| `AccountRef.value` | body | `string` | no | — |
| `MainContact` | body | `object` | no | — |
| `MainContact.Email` | body | `object` | no | — |
| `MainContact.Email.value` | body | `string` | no | — |
| `MainContact.Phone1` | body | `object` | no | — |
| `MainContact.Phone1.value` | body | `string` | no | — |
| `MainContact.Address` | body | `object` | no | — |
| `MainContact.Address.AddressLine1` | body | `object` | no | — |
| `MainContact.Address.AddressLine1.value` | body | `string` | no | — |
| `MainContact.Address.AddressLine2` | body | `object` | no | — |
| `MainContact.Address.AddressLine2.value` | body | `string` | no | — |
| `MainContact.Address.City` | body | `object` | no | — |
| `MainContact.Address.City.value` | body | `string` | no | — |
| `MainContact.Address.State` | body | `object` | no | — |
| `MainContact.Address.State.value` | body | `string` | no | — |
| `MainContact.Address.PostalCode` | body | `object` | no | — |
| `MainContact.Address.PostalCode.value` | body | `string` | no | — |
| `MainContact.Address.Country` | body | `object` | no | — |
| `MainContact.Address.Country.value` | body | `string` | no | — |
