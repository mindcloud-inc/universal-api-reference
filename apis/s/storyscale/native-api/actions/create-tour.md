# Create Tour with Storyscale

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tour/create/`
- **Base URL:** `https://prodapi.storyscale.com/api`
- **Official documentation:** [Create Tour](https://prodapi.storyscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversion_enabled` | body | `boolean` | no | Whether conversion tracking is enabled for the tour. |
| `description` | body | `string` | no | Description of the tour. |
| `is_active` | body | `boolean` | no | Whether the tour is active. |
| `is_published` | body | `boolean` | no | Whether the tour is published. |
| `is_template` | body | `boolean` | no | Whether the tour is a template. |
| `name` | body | `string` | no | Name of the tour. |
