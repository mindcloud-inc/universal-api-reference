# Create Direct Verification with IdentityCheck

## Endpoint

- **Method:** `POST`
- **Path:** `/direct-verification`
- **Base URL:** `https://identity.stackgo.io/api`
- **Official documentation:** [Create Direct Verification](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | body | `string` | no | Optional upstream contact identifier. |
| `email` | body | `string` | yes | Email address for the verification invite. |
| `emailUser` | body | `string` | no | Whether IdentityCheck should email the user. |
| `firstName` | body | `string` | no | First name of the person to verify. |
| `lastName` | body | `string` | no | Last name of the person to verify. |
| `triggeredBy` | body | `string` | no | Source label for how the verification was triggered. |
