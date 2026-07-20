# Update Issue with Fleetio

Updates an existing issue in Fleetio.

## Endpoint

- **Method:** `PATCH`
- **Path:** `issues/:id`
- **Base URL:** `https://secure.fleetio.com/api/`
- **Official documentation:** [Update Issue](https://developer.fleetio.com/docs/api/issues-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the relevant record |
| `asset_id` | body | `number` | no | The ID of the asset associated with the Issue. |
| `asset_type` | body | `string` | no | The type of the asset associated with the Issue. |
| `summary` | body | `string` | no | A short summary of the Issue. |
| `description` | body | `string` | no | A longer description of the Issue. |
| `reported_by_id` | body | `number` | no | The id of the `Contact` who reported this Issue. |
| `reported_at` | body | `date` | no | The date and time this Issue is reported. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `issue_priority_id` | body | `number` | no | The id of the associated `IssuePriority` for this Issue. |
| `number` | body | `number` | no | A unique identifier for the Issue. |
| `due_date` | body | `date` | no | The date on which this Issue should be resolved by. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `due_meter_value` | body | `number` | no | The meter value at which this Issue should be resolved by. |
| `due_secondary_meter_value` | body | `number` | no | The secondary meter value at which this Issue should be resolved by. |
| `fault_id` | body | `number` | no | The id of the `Fault` associated with this Issue. |
| `custom_fields` | body | `object` | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
| `meter_entry_attributes` | body | `object` | no | An Issue may be associated with a [Meter Entry](/docs/api/meter-entries). |
| `secondary_meter_entry_attributes` | body | `object` | no | An Issue may be associated with a secondary [Meter Entry](/docs/api/meter-entries). |
| `comments_attributes` | body | `array<object>` | no | — |
| `documents_attributes` | body | `array<object>` | no | An array of one or more document objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |
| `images_attributes` | body | `array<object>` | no | An array of one or more image objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |
| `assigned_contact_ids` | body | `array<number>` | no | An array of ids of assigned `Contacts` related to the Issue. |
| `label_ids` | body | `array<number>` | no | — |
