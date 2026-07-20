# Match a standardization to a list of candidates with DocuPipe

Matches a standardization to candidates in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/enterprise/matching`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Match a standardization to a list of candidates](https://docs.docupipe.ai/reference/match_standardization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `standardizationId` | body | `string` | yes | The id of the standardization you're looking to match |
| `matchCandidates[]` | body | `array<object>` | yes | — |
| `instructions` | body | `string` | yes | The instructions for the match |
