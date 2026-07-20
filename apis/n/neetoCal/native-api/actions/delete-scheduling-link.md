# Delete Scheduling Link with NeetoCal

Deletes an existing scheduling link from NeetoCal.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/meetings/:meeting_sid`
- **Base URL:** `https://{subdomain}.neetocal.com/api/external/v2`
- **Official documentation:** [Delete Scheduling Link](https://apidocs.neetocal.com/api-reference/scheduling-links/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meeting_sid` | path | `string` | yes | The scheduling link SID. |
