# Create Case Tag with FuseDesk

Creates a new case tag in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/casetags`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Create Case Tag](https://documenter.getpostman.com/view/11014835/SztBc8ix#05f9241b-de05-4355-960e-74c194639017)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagname` | body | `string` | yes | The case tag name to create. |
