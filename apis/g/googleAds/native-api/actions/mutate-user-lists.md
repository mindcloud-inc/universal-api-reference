# Mutate User Lists with Google Ads

Creates, updates, or removes user lists in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/userLists:mutate`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Mutate User Lists](https://developers.google.com/google-ads/api/reference/rpc/v22/UserListService/MutateUserLists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `operations[]` | body | `array<object>` | yes | Mutation operations array for user lists. |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
