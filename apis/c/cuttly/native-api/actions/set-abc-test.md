# Set ABC Test with Cutt.ly

Sets an ABC test for a shortened link in Cutt.ly.

## Endpoint

- **Method:** `GET`
- **Path:** `/api.php`
- **Base URL:** `https://cutt.ly/api`
- **Official documentation:** [Set ABC Test](https://cutt.ly/api-documentation/cuttly-links-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edit` | query | `string` | yes | The short link to edit. |
| `abtest_b` | query | `number` | yes | Traffic percentage to send to variation B. |
| `abtest_bvariation` | query | `string` | yes | Destination URL for variation B. |
| `abtest_c` | query | `number` | yes | Traffic percentage to send to variation C. |
| `abtest_cvariation` | query | `string` | yes | Destination URL for variation C. |
