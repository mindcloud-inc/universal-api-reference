# Create Person with OneSuite

Creates a person in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/people`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Create Person](https://rest-api.onesuite.io/#create-people-with-all-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Full name of the person from the official create-people docs. |
| `companyId` | body | `string` | no | Optional company ID to associate with the person at creation time. |
