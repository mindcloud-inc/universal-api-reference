# List Awardees with HigherGov

Retrieves awardees from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/awardee/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List Awardees](https://www.highergov.com/api-external/docs/#/api-external/api_external_awardee_list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `awardee_key_parent` | query | `string` | no | HigherGov Awardee Key at parent level |
| `cage_code` | query | `string` | no | CAGE code |
| `primary_naics` | query | `string` | no | Primary registered NAICS code |
| `registration_last_update_date` | query | `string` | no | Date the awardee last updated its SAM registration |
| `uei` | query | `string` | no | Unique Entity ID |
