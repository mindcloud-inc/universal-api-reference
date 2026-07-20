# Solve Rule with Rulebricks

Executes a rule in Rulebricks.

## Endpoint

- **Method:** `POST`
- **Path:** `/solve/:slug`
- **Base URL:** `https://rulebricks.com/api/v1`
- **Official documentation:** [Solve Rule](https://rulebricks.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique slug of the rule to execute |
