# Commission Lead with leadtributor.cloud

Creates a commission for a lead in leadtributor.cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/:leadId/commissions`
- **Base URL:** `https://api.leadtributor.cloud`
- **Official documentation:** [Commission Lead](https://developer.leadtributor.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | path | `string` | yes | ID of the lead to commission. |
| `salesPartnerId` | body | `string` | yes | Sales partner ID that should receive the lead commission. |
| `salesPipelineId` | body | `string` | yes | Sales pipeline ID for the lead commission. |
