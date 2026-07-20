# Generate Recipient Proof with PostcardMania

Creates a proof for a PostcardMania recipient.

## Endpoint

- **Method:** `POST`
- **Path:** `/recipient/{{recipientId}}/generate-proof`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Generate Recipient Proof](https://docs.pcmintegrations.com/docs/directmail-api/b3ynzdasfi2mw)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientId` | path | `number` | yes | Internal recipient identifier. |
