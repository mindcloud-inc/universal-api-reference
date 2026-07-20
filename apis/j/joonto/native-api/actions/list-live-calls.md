# List Live Calls with Joonto

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Live/Calls/:filter`
- **Base URL:** `https://api.joonto.com`
- **Official documentation:** [List Live Calls](https://api.joonto.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filter` | path | `string` | yes |
| `managers[]` | body | `array<string>` | no |
| `users[]` | body | `array<string>` | no |
| `callTypes[]` | body | `array<string>` | no |
