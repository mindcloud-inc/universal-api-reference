# Delete Contact with DialMyCalls

Deletes an existing contact from DialMyCalls.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contact/:ContactId`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Delete Contact](https://www.dialmycalls.com/api-documentation#contact-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ContactId` | path | `string` | yes | The DialMyCalls contact ID to delete. |
