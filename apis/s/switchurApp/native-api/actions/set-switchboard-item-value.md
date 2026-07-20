# Set Switchboard Item Value with Switchur App

## Endpoint

- **Method:** `PUT`
- **Path:** `/:setToValue/{switchboardItemToken}`
- **Base URL:** `https://api.switchur.com/`
- **Official documentation:** [Set Switchboard Item Value](https://support.switchur.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setToValue` | path | `string` | yes | Value to set for the Switchboard item. For a switch, use on, off, or toggle; counters and keywords use the value accepted by the item type. |
