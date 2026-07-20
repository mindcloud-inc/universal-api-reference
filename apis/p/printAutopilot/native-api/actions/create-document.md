# Create Document with Print Autopilot

Creates a document in Print Autopilot from a base64 PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/document/create`
- **Base URL:** `https://printautopilot.com/api`
- **Official documentation:** [Create Document](https://documenter.getpostman.com/view/1334461/TW6wJonb#99ca43c2-821e-471f-8530-e562bfbe642b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileName` | body | `string` | no | PDF file name. |
| `base64` | body | `string` | yes | Base64-encoded PDF content. |
