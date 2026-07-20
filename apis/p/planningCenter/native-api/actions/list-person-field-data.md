# List Person Field Data with Planning Center

Retrieves field data for a person in Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/people/:person_id/field_data`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List Person Field Data](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/person)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person_id` | path | `string` | yes | The person id. |
| `include` | query | `string` | no | Include associated field_definition, field_option, or tab records in the response. |
| `order` | query | `string` | no | Sort field data by a supported field; prefix the field with a hyphen for descending order. |
| `where` | query | `object` | no | Field-qualified field data query filters. |
| `where[field_definition_id]` | query | `number` | no | Query field data by an exact related field_definition id. |
| `where[file]` | query | `string` | no | Query field data by an exact file value. |
| `where[file_content_type]` | query | `string` | no | Query field data by an exact file_content_type value. |
| `where[file_name]` | query | `string` | no | Query field data by an exact file_name value. |
| `where[file_size]` | query | `number` | no | Query field data by an exact file_size value. |
| `where[value]` | query | `string` | no | Query field data by an exact value. |
