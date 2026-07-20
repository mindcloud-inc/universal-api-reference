# Update Lead Campaign Status with LinkedCamp

## Endpoint

- **Method:** `PUT`
- **Path:** `/leads/:leadId`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Update Lead Campaign Status](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | path | `string` | yes | Lead identifier. |
| `status` | query | `string` | yes | Lead campaign status action: RESUME, PAUSE, or DELETE. |
