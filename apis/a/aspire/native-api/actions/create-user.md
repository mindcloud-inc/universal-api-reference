# Create User with Aspire

Retrieves pay codes from your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `Users`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create User](https://guide.youraspire.com/apidocs/users-8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | yes | — |
| `AllBranchAccess` | body | `boolean` | yes | — |
| `BranchAccess` | body | `array<number>` | no | — |
| `ExternalContactReference` | body | `list<string>` | yes | Maximum length: 255. |
| `Password` | body | `string` | yes | Maximum length: 500. |
| `UserRoles` | body | `array<number>` | yes | — |
| `VerifyPassword` | body | `string` | no | Maximum length: 500. |
