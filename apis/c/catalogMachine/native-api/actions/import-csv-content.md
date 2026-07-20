# Import CSV Content with Catalog Machine

Starts a CSV import job in Catalog Machine.

## Endpoint

- **Method:** `POST`
- **Path:** `/import/csv`
- **Base URL:** `https://www.catalogmachine.com/api/v1`
- **Official documentation:** [Import CSV Content](https://help.catalogmachine.com/en/articles/3667421-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `csv` | body | `string` | yes | CSV content payload. |
