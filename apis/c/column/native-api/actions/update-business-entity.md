# Update Business Entity with Column

## Endpoint

- **Method:** `PATCH`
- **Path:** `/entities/business/:entity_id`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Update Business Entity](https://column.com/docs/api/#entity/update-business)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | path | `string` | yes | — |
| `business_name` | body | `string` | no | — |
| `ein` | body | `string` | no | — |
| `industry` | body | `string` | no | — |
| `website` | body | `string` | no | — |
| `dba_name` | body | `string` | no | — |
| `legal_type` | body | `list` | no | Accepted values: `Corporation`, `General Partnership`, `Government`, `LLC`, `Limited Partnership`, `Non-Profit`, `Other`, `Professional Association`, `Sole Proprietorship`, `Trust`. |
