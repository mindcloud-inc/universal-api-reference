# Get member (OData) with Bridge Interactive Platform

Retrieves a member from Bridge Interactive Platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/OData/:dataset/Member(':MemberKey')`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get member (OData)](https://bridgedataoutput.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Bridge dataset code. This tenant was validated against dataset test. |
| `MemberKey` | path | `string` | yes | OData member identifier from Bridge. |
