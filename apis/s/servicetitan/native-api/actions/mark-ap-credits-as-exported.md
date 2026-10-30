# Mark AP Credits as Exported with ServiceTitan

Marks the specified AP credits as exported in ServiceTitan.

## Endpoint

- **Method:** `POST`
- **Path:** `accounting/v2/tenant/{tenant}/ap-credits/markasexported`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Mark AP Credits as Exported](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/ApCredits_MarkAsExported)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `apCredits[]` | body | `array<object>` | no |
| `apCredits[].apCreditId` | body | `list<number>` | yes |
