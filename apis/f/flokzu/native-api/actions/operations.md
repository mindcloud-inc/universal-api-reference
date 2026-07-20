# Operations with Flokzu

## Endpoint

- **Method:** `POST`
- **Path:** `/commons/MATH/operations`
- **Base URL:** `https://app.flokzu.com/flokzuopenapi/api`
- **Official documentation:** [Operations](https://flokzu.docs.apiary.io/reference/commons/operations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `oper` | query | `string` | yes | Operation code from Flokzu docs: sum, concat, or contains. |
| `elem_1` | body | `string` | yes | First input element for the selected operation. |
| `elem_2` | body | `string` | yes | Second input element for the selected operation. |
| `elem_N` | body | `string` | no | Optional additional input element for the selected operation. |
