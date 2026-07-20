# Get Form Analytics with Florm

Retrieves analytics for a Florm form.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/analytics/form/:form_guid`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Get Form Analytics](https://api.florm.io/docs#/default/form_analytics_v1_analytics_form__form_guid__post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_guid` | path | `string` | yes | GUID of the Florm form to analyze. |
