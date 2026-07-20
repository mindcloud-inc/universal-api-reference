# List Application Numbers with DailyMed

Retrieves application numbers from DailyMed.

## Endpoint

- **Method:** `GET`
- **Path:** `/applicationnumbers.json`
- **Base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`
- **Official documentation:** [List Application Numbers](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/applicationnumbers_api.cfm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `application_number` | query | `string` | no | Application number of a drug. |
| `marketing_category_code` | query | `string` | no | Marketing category code of a drug. |
| `setid` | query | `string` | no | Set ID of a label. |
