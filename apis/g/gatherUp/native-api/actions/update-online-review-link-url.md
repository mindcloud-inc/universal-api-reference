# Update Online Review Link URL with GatherUp

Updates an online review link URL in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/business/online-review-link/update`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Update Online Review Link URL](https://app.gatherup.com/api/doc/business/online-review-link/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | yes | Business id. |
| `link` | body | `string` | yes | Online review link URL. |
| `type` | body | `string` | yes | Online review link type. |
