# Get Dashboard Call Summary with Joonto

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Dashboard/CallSummary/:filter`
- **Base URL:** `https://api.joonto.com`
- **Official documentation:** [Get Dashboard Call Summary](https://api.joonto.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filter` | path | `string` | yes |
| `managers[]` | body | `array<string>` | no |
| `users[]` | body | `array<string>` | no |
| `callTypes[]` | body | `array<string>` | no |
