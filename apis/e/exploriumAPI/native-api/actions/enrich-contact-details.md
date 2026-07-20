# Enrich Contact Details with Explorium

Enriches prospects with contact details in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/prospects/contacts_information/enrich`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Enrich Contact Details](https://developers.explorium.ai/reference/prospects/enrichments/contacts_information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prospect_id` | body | `string` | yes | The Explorium prospect identifier to enrich. |
