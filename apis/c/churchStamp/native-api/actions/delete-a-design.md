# Delete a Design with ChurchStamp

Deletes an existing design from ChurchStamp by design ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/delete-design`
- **Base URL:** `https://v2.churchstamp.com/api/1.1/wf`
- **Official documentation:** [Delete a Design](https://churchstampapi.docs.apiary.io/reference/designs/delete-a-design)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `design_id` | body | `string` | yes | Unique identifier for the design to delete. |
