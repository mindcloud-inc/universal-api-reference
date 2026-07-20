# Rename Reviewer Group with Filestage

Updates a reviewer group name in Filestage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/steps/{stepId}/name`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Rename Reviewer Group](https://developers.filestage.io/docs/api/hi66jjtl28qwg-rename-reviewer-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stepId` | path | `string` | yes | Step Id |
| `name` | body | `string` | no | The new name for the reviewer group. |
