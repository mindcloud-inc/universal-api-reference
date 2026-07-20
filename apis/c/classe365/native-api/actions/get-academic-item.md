# Get Academic Item with Classe365

Retrieves an academic item from Classe365 by type and ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/getAcademicDataForParticular`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Get Academic Item](https://speca.io/classe365/academics#get-data-for-a-particular-department-class-section-or-subject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Academic entity id to fetch. |
| `type` | query | `string` | no | Entity type such as class, section, or subject. |
