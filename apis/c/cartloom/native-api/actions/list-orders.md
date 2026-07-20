# List Orders with Cartloom

Retrieves multiple order records from Cartloom.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/list/format/json`
- **Base URL:** `https://mindcloudstage0424.cartloom.com/api`
- **Official documentation:** [List Orders](https://support.cartloom.com/hc/en-us/articles/115000892907-List-Orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | body | `date` | yes | Start date in YYYY-MM-DD format. |
| `end_date` | body | `date` | yes | End date in YYYY-MM-DD format. |
| `search_type` | body | `list` | no | Search type, either email or last_name. Accepted values: `0`, `1`. |
| `keyword` | body | `string` | no | Keyword value for the selected search type. |
