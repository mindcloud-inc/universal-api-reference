# Add Online Review Link with GatherUp

Adds an online review link in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/business/online-review-link/add`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Add Online Review Link](https://app.gatherup.com/api/doc/business/online-review-link/add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | yes | Business id. |
| `link` | body | `string` | yes | Online review link URL. |
| `type` | body | `string` | yes | Online review link type. |
