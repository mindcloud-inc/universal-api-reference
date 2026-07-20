# Create Organisation with smsmode

## Endpoint

- **Method:** `POST`
- **Path:** `commons/v1/organisations`
- **Base URL:** `https://rest.smsmode.com/`
- **Official documentation:** [Create Organisation](https://dev.smsmode.com/commons/v1/#tag/Organisation/operation/organisation-creation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name request body field documented by the smsmode API. |
| `contact` | body | `object` | yes | Contact request body field documented by the smsmode API. |
| `address` | body | `object` | no | Address request body field documented by the smsmode API. |
| `billingContact` | body | `object` | no | Billing Contact request body field documented by the smsmode API. |
| `billingAddress` | body | `object` | no | Billing Address request body field documented by the smsmode API. |
| `companyInformation` | body | `object` | no | Company Information request body field documented by the smsmode API. |
| `balance` | body | `object` | no | Balance request body field documented by the smsmode API. |
| `monthlyConsumptionLimit` | body | `number` | no | Monthly Consumption Limit request body field documented by the smsmode API. |
