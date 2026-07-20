# Ingest Traces (OTLP) with PromptLayer Run Agent

Ingests trace data into PromptLayer using OTLP.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/traces`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Ingest Traces (OTLP)](https://docs.promptlayer.com/reference/otlp-ingest-traces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceSpans[]` | body | `array<object>` | yes | OTLP ExportTraceServiceRequest resourceSpans payload in JSON encoding. |
