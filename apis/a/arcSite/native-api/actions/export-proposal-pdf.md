# Export Proposal PDF with ArcSite

Exports a proposal PDF for an ArcSite drawing.

## Endpoint

- **Method:** `POST`
- **Path:** `/export_proposal_pdf`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Export Proposal PDF](https://dev.arcsite.com/#export-proposal-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | Template ID from proposal templates. |
| `drawing_id` | body | `string` | yes | Drawing ID to export. |
