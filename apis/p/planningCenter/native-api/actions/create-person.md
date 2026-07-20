# Create Person with Planning Center

Creates a new person in Planning Center.

## Endpoint

- **Method:** `POST`
- **Path:** `/people/v2/people`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [Create Person](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | JSON:API resource object containing the Person type, attributes, and optional relationships. |
| `include` | query | `string` | no | — |
