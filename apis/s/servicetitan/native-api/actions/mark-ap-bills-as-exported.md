# Mark AP Bills as Exported with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `accounting/v2/tenant/{tenant}/ap-bills/markasexported`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Mark AP Bills as Exported](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/ApBills_MarkAsExported)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billIds[]` | body | `array<number>` | yes | AP bill IDs to mark as exported. |
