# Lookup Phone Number with Lasso X

Finds a phone number in Lasso X by number.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/teledata/:phoneNumber`
- **Base URL:** `https://api.lassox.com`
- **Official documentation:** [Lookup Phone Number](https://docs.lassox.com/data-apis/teledata/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | path | `string` | yes | Phone number to look up. |
| `includeCompany` | query | `boolean` | no | Whether to include company details in the phone lookup. |
