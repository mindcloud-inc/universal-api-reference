# Create Location with TalentHR

Creates a new location in TalentHR.

## Endpoint

- **Method:** `POST`
- **Path:** `/locations`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [Create Location](https://apidocs.talenthr.io/#44d36dd5-8845-4098-957e-c79ce5d12ff0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Location name. |
| `field_data` | body | `object` | yes | Location field data object with address and is_remote. |
