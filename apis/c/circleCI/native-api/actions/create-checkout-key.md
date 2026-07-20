# Create Checkout Key with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:project_slug/checkout-key`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Create Checkout Key](https://circleci.com/docs/api/v2/#tag/Checkout-Key/operation/createCheckoutKey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
| `type` | body | `string` | no | Checkout key type. |
