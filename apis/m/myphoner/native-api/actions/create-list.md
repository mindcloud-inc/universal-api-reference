# Create List with Myphoner

Creates a new list in Myphoner.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists`
- **Base URL:** `https://{subdomain}.myphoner.com/api/v2`
- **Official documentation:** [Create List](https://www.myphoner.com/docs/api/#lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Script or description for the list. |
| `name` | body | `string` | yes | The name of the new Myphoner list. |
