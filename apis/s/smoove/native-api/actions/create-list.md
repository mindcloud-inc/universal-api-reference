# Create List with Smoove

Creates a new contact list in Smoove.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/Lists`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [Create List](https://rest.smoove.io)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `publicName` | body | `string` | no |
| `description` | body | `string` | no |
| `publicDescription` | body | `string` | no |
| `permissions.isPublic` | body | `boolean` | no |
| `permissions.allowsUsersToSubscribe` | body | `boolean` | no |
| `permissions.allowsUsersToUnsubscribe` | body | `boolean` | no |
| `permissions.isPortal` | body | `boolean` | no |
