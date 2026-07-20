# Get Form Analytics Summary with Florm

Retrieves analytics summary for a Florm form.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/analytics/form/:form_guid/summary`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Get Form Analytics Summary](https://api.florm.io/docs#/default/form_summary_v1_analytics_form__form_guid__summary_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_guid` | path | `string` | yes | GUID of the Florm form to summarize. |
