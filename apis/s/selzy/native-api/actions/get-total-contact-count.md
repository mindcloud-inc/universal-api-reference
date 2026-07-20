# Get Total Contact Count with Selzy

Retrieves the total contact count for a Selzy user.

## Endpoint

- **Method:** `POST`
- **Path:** `getTotalContactsCount`
- **Base URL:** `https://api.selzy.com/en/api`
- **Official documentation:** [Get Total Contact Count](https://selzy.com/en/support/api/contacts/gettotalcontactscount/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `login` | query | `string` | yes | Selzy user login, as shown in the Selzy account, not necessarily the email address. |
