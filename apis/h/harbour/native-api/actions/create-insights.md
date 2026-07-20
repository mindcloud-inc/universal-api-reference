# Create Insights with Harbour

Creates document insights from completed documents, drafts, or URLs in Harbour.

## Endpoint

- **Method:** `POST`
- **Path:** `/insights`
- **Base URL:** `https://api.myharbourshare.com/v2`
- **Official documentation:** [Create Insights](https://developers.harbourshare.com/v2#create-insights)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draft_id` | body | `string` | no | Harbour draft document identifier. Provide one of draft_id, completed_id, doc_text, or url. |
| `completed_id` | body | `string` | no | Harbour completed agreement asset identifier. Provide one of draft_id, completed_id, doc_text, or url. |
| `doc_text` | body | `string` | no | Raw document text to analyze. Provide one of draft_id, completed_id, doc_text, or url. |
| `url` | body | `string` | no | Publicly accessible document URL to analyze. Provide one of draft_id, completed_id, doc_text, or url. |
| `context` | body | `string` | yes | Background context the model can use while generating insights. |
| `insights[]` | body | `array<object>` | yes | List of Harbour insight request objects, for example [{ "type": "document_title" }, { "type": "contract_values" }]. |
| `stream` | body | `boolean` | yes | Whether Harbour should stream the insight generation response. |
