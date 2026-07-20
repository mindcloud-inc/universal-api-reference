# Enrich Contact with Zoominfo

Enriches a contact with ZoomInfo data.

## Endpoint

- **Method:** `POST`
- **Path:** `enrich/contact`
- **Base URL:** `https://api.zoominfo.com/`
- **Official documentation:** [Enrich Contact](https://api-docs.zoominfo.com/#c145dd01-eb54-4fc2-bbdb-9edc04b7ea1b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `matchPersonInput[]` | body | `array<object>` | yes | Array of contact match objects. Each object can include fields such as personId, fullName, firstName, lastName, emailAddress, phone, companyId, or companyName. |
| `outputFields[]` | body | `array<string>` | no | Array of response field names to return. Send multiple values as a array. |
