# Get Contact with Umbler Talk

Retrieves a contact from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/[:id]/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Get Contact](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The contact ID. |
| `organizationId` | query | `string` | yes | The organization ID. |
