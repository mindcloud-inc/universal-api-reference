# Move Articles To Group with Productlane

Moves help center articles to a Productlane doc group.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs/groups/move-articles`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Move Articles To Group](https://productlane.mintlify.dev/docs/api/docs/move-articles-to-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `articleIds[]` | body | `array<string>` | yes | One or more doc article IDs to move. |
| `groupId` | body | `string` | yes | Target docs group ID, or null to ungroup. |
