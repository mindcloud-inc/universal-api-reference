# Create Invitation Link with ProvenExpert

Creates a personal survey invitation link in ProvenExpert.

## Endpoint

- **Method:** `POST`
- **Path:** `/invite/url/create`
- **Base URL:** `https://www.provenexpert.com/api/v1`
- **Official documentation:** [Create Invitation Link](https://developer.provenexpert.com/index_en.html#invite-url-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.code` | body | `string` | yes | Survey code for which the personal invitation link should be created. |
| `data.email` | body | `string` | yes | Email address of the evaluator. |
| `data.name` | body | `string` | no | Name of the evaluator. |
