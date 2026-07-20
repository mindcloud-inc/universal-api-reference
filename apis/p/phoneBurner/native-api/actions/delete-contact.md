# Delete Contact with PhoneBurner

Deletes an existing contact from PhoneBurner.

## Endpoint

- **Method:** `DELETE`
- **Path:** `rest/1/contacts/{{contactId}}`
- **Base URL:** `https://www.phoneburner.com/`
- **Official documentation:** [Delete Contact](https://www.phoneburner.com/developer/route_list#contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | no | The PhoneBurner contact id. |
| `permanent` | query | `string` | no | Set to 1 to permanently delete instead of moving to trash. |
