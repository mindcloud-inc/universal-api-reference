# Create Proposal Cover with Better Proposals

Creates a proposal cover in Better Proposals.

## Endpoint

- **Method:** `POST`
- **Path:** `/proposal/cover/create`
- **Base URL:** `https://api.betterproposals.io`
- **Official documentation:** [Create Proposal Cover](https://betterproposals.io/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BrandID` | body | `string` | no | Brand ID. If omitted, Better Proposals uses the brand settings defaults. |
| `CoverName` | body | `string` | no | Cover name. Default is Untitled. |
| `BGColour` | body | `string` | no | Background colour value. Default is 111111. |
| `Headline` | body | `string` | no | Cover headline. Default is Proposal for _________. |
| `Subheader` | body | `string` | no | Cover subheader. Default is Written by ________ for ________. |
| `TextColour` | body | `string` | no | Text colour value. Default is ffffff. |
| `TextAlign` | body | `string` | no | Text alignment. Default is left. |
| `ButtonStyle` | body | `string` | no | Button style. Default is round. |
| `ButtonText` | body | `string` | no | Button text. Default is Start Reading Proposal. |
