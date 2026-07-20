# Create Action with NextLead

Creates a new task in NextLead.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/receive/actions/create-action`
- **Base URL:** `https://dashboard.nextlead.app`
- **Official documentation:** [Create Action](https://dashboard.nextlead.app/en/api-documentation#receive-action-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | Action title. |
| `column` | body | `string` | yes | Action column identifier. |
