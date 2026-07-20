# Create automation condition with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/automation`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create automation condition](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace` | body | `string` | no |
| `createdBy` | body | `string` | no |
| `eventType` | body | `string` | no |
| `trigger` | body | `object` | no |
| `events[]` | body | `array` | no |
| `actions[]` | body | `array` | no |
| `description` | body | `string` | no |
| `isActive` | body | `boolean` | no |
| `isTrashed` | body | `boolean` | no |
