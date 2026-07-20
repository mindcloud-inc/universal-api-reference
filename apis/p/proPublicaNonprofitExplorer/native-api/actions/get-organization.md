# Get Organization with ProPublica Nonprofit Explorer

Retrieves an organization from ProPublica Nonprofit Explorer by EIN.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{ein}}.json`
- **Base URL:** `https://projects.propublica.org/nonprofits/api/v2`
- **Official documentation:** [Get Organization](https://projects.propublica.org/nonprofits/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ein` | path | `string` | yes | Integer employer identification number for the organization, without a dash. Leading zeroes are trimmed by the API. |
