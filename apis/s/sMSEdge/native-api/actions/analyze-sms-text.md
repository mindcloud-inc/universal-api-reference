# Analyze SMS Text with SMSEdge

Analyzes SMS text before sending in SMSEdge.

## Endpoint

- **Method:** `POST`
- **Path:** `/text/analyze/`
- **Base URL:** `https://api.smsedge.com/v1`
- **Official documentation:** [Analyze SMS Text](https://developers.smsedge.io/reference/text-analyze)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | Text of SMS you want to verify before sending |
