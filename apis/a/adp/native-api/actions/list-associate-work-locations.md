# List Associate Work Locations with ADP

Associate Work Locations

## Endpoint

- **Method:** `GET`
- **Path:** `/hcm/v1/validation-tables/associate-work-locations`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [List Associate Work Locations](https://api-central.adp.com/projects/735093bcc595cb7d5328f9fb6494a4bec696ce0fb6a0f33f)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | **Examples:** - /mobileUserAccounts/associateOID eq 'G4O73G9Z62SL2NFM'  - /mobileUserAccounts/organizationOID eq 'ABCDEFGH' - /mobileUserAccounts/accountStatusCode eq 'STATCODE' - /mobileUserAccounts/personName/givenName eq 'John' - /mobileUserAccounts/personName/familyName1 eq 'Smith' - /mobileUserAccounts/birthDate eq '01-01-1970' |
