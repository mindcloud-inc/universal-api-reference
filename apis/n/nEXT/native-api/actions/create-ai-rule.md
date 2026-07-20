# Create AI Rule with NEXT

Creates a new AI rule in NEXT.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai-rules`
- **Base URL:** `https://rest.eu-west-1.nextapp.co/v1`
- **Official documentation:** [Create AI Rule](https://developer.nextapp.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The AI rule name. |
| `type` | body | `string` | yes | The AI rule type. |
| `status` | body | `string` | yes | The AI rule status. |
| `data` | body | `string` | yes | The AI rule definition payload. |
