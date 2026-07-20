# Create Research Task with Tavily

Creates a research task in Tavily.

## Endpoint

- **Method:** `POST`
- **Path:** `/research`
- **Base URL:** `https://api.tavily.com`
- **Official documentation:** [Create Research Task](https://docs.tavily.com/documentation/api-reference/endpoint/research)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `citation_format` | body | `string` | no | Citation format. Accepted values are numbered, mla, apa, or chicago. |
| `input` | body | `string` | yes | The research task or question to investigate. |
| `model` | body | `string` | no | Research model. Accepted values are mini, pro, or auto. |
| `output_schema` | body | `object` | no | Optional JSON Schema object that defines the research output shape. |
