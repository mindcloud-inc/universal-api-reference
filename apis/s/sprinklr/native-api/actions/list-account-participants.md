# List Account Participants with Sprinklr

Retrieves account participants from Sprinklr.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v2/account/all-participants/{accountId}`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [List Account Participants](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Faccount%2Fall-participants%2F%7BaccountId%7D/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `number` | yes |
| `clientId` | query | `string` | yes |
