# Set Unique Clicks with Cutt.ly

Sets the unique-click window for a shortened link in Cutt.ly.

## Endpoint

- **Method:** `GET`
- **Path:** `/api.php`
- **Base URL:** `https://cutt.ly/api`
- **Official documentation:** [Set Unique Clicks](https://cutt.ly/api-documentation/cuttly-links-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edit` | query | `string` | yes | The short link to edit. |
| `unique` | query | `number` | yes | Custom uniqueness window in minutes (15-1440 for Team plans). |
