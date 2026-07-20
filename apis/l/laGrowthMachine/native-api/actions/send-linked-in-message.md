# Send LinkedIn Message with LaGrowthMachine

Sends a LinkedIn message to a lead in LaGrowthMachine.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/linkedin`
- **Base URL:** `https://apiv2.lagrowthmachine.com/flow`
- **Official documentation:** [Send LinkedIn Message](https://documenter.getpostman.com/view/2071164/TVCmSkH2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audioUrl` | body | `string` | no | Direct download URL to an MP3 voice message. Provide either audio URL or message. |
| `identityId` | body | `string` | yes | Identity ID used to send the LinkedIn message. |
| `leadId` | body | `string` | no | Target lead ID. Provide either Lead ID or LinkedIn URL. |
| `linkedinUrl` | body | `string` | no | Target lead LinkedIn URL. Provide either Lead ID or LinkedIn URL. |
| `memberId` | body | `string` | yes | Member ID associated with the sender. Required by the provider. |
| `message` | body | `string` | no | LinkedIn message text. Provide either message or audio URL. |
