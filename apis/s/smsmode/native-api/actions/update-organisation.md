# Update Organisation with smsmode

## Endpoint

- **Method:** `PATCH`
- **Path:** `commons/v1/organisations/:organisationId`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Update Organisation](https://dev.smsmode.com/commons/v1/#tag/Organisation/operation/organisation-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationId` | path | `string` | yes | Organisation ID path parameter from the smsmode API route. |
| `contact` | body | `object` | no | Contact request body field documented by the smsmode API. |
| `address` | body | `object` | no | Address request body field documented by the smsmode API. |
| `billingContact` | body | `object` | no | Billing Contact request body field documented by the smsmode API. |
| `billingAddress` | body | `object` | no | Billing Address request body field documented by the smsmode API. |
| `companyInformation` | body | `object` | no | Company Information request body field documented by the smsmode API. |
