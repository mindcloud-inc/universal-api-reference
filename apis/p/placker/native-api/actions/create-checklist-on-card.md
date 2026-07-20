# Create Checklist On Card with Placker

## Endpoint

- **Method:** `POST`
- **Path:** `/card/:card/checklist`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Create Checklist On Card](https://placker.com/docs/api/paths/card.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card` | path | `number` | yes | Card ID. |
| `title` | body | `string` | yes | Title of the checklist. |
| `position` | body | `number` | no | Position of the checklist. |
