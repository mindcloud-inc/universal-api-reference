# Assign User with Wati

Updates a conversation assignment in Wati.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/assignOperator`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [Assign User](https://docs.wati.io/reference/post_api-v1-assignoperator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address of the operator to assign. |
| `whatsappNumber` | query | `string` | yes | Target WhatsApp phone number for the assignment. |
