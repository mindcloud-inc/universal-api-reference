# Get Employee Photo with BambooHR

Retrieves employee photo from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/employees/:employeeId/photo/:size`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Employee Photo](https://documentation.bamboohr.com/reference/get-employee-photo)

## Requirements

- **OAuth scopes:** `employee:photo`
- **scope:** `employee:photo` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeId` | path | `number` | yes | The ID of the employee whose photo to retrieve. |
| `size` | path | `list<string>` | yes | The desired photo size. One of: `original`, `large`, `medium`, `small`, `xs`, `tiny`. Accepted values: `large`, `medium`, `original`, `small`, `tiny`, `xs`. |
| `width` | query | `number` | no | Optional. Scales the returned image to the specified pixel width, capped at the natural width of the requested size. Only applies to `small` and `tiny` sizes. |
| `height` | query | `number` | no | Optional. Scales the returned image to the specified pixel height, capped at the natural height of the requested size. Only applies to `small` and `tiny` sizes. |
| `If-None-Match` | header | `string` | no | Optional. The `ETag` value from a previous response for this same photo. If it still matches, the server returns `304 Not Modified` with no body instead of re-sending the image. |
