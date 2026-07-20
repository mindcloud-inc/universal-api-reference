# Update User with Aspire

Modify an existing users Branch Access and Role. Optionally specify a new Password.

## Endpoint

- **Method:** `PUT`
- **Path:** `Users`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update User](https://guide.youraspire.com/apidocs/users-7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | yes | Format: `text`. |
| `AllBranchAccess` | body | `boolean` | yes | Format: `text`. |
| `BranchAccess` | body | `array<number>` | no | Specify the specific Branch Access for this user. `All Branch Access` must be toggled off otherwise this value is overwritten. |
| `Password` | body | `string` | no | Optionally set a new password for the user. |
| `UserID` | body | `list` | yes | — |
| `UserRoles` | body | `array<number>` | no | — |
