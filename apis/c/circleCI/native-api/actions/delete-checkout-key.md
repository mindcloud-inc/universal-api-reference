# Delete Checkout Key with CircleCI

## Endpoint

- **Method:** `DELETE`
- **Path:** `/project/:project_slug/checkout-key/:fingerprint`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Delete Checkout Key](https://circleci.com/docs/api/v2/#tag/Checkout-Key/operation/deleteCheckoutKey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fingerprint` | path | `string` | no | Checkout key fingerprint. |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
