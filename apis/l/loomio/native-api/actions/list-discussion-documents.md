# List Discussion Documents with Loomio

Retrieves documents from a Loomio discussion.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/for_discussion`
- **Base URL:** `https://www.loomio.com/api/v1`
- **Official documentation:** [List Discussion Documents](https://github.com/loomio/loomio/blob/master/app/controllers/api/v1/documents_controller.rb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `discussion_id` | query | `string` | no | The Loomio discussion ID to list documents for. |
