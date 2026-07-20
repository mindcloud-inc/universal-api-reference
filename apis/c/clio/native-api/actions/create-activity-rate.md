# Create Activity Rate with Clio Manage

Creates a new activity rate in Clio Manage.

## Endpoint

- **Method:** `POST`
- **Path:** `/activity_rates.json`
- **Base URL:** `https://app.clio.com/api/v4`
- **Official documentation:** [Create Activity Rate](https://docs.developers.clio.com/clio-manage/api-reference/#tag/Activity%20Rates/operation/ActivityRate%23create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.contact_id` | body | `number` | yes | Contact associated with this activity rate. |
| `data.rate` | body | `number` | yes | Hourly or flat monetary rate. |
| `data.flat_rate` | body | `boolean` | no | Whether this rate should be treated as a flat rate. |
