# Match a standardization to a list of candidates with DocuPanda - Document Understanding

Creates a standardization match in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/enterprise/matching`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Match a standardization to a list of candidates](https://docs.docupipe.ai/reference/match_standardization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instructions` | body | `string` | yes | The instructions for the match |
| `matchCandidates` | body | `list<string>` | yes | — |
| `standardizationId` | body | `string` | yes | The id of the standardization you're looking to match |
| `matchCandidates[]` | body | `array<object>` | yes | — |
