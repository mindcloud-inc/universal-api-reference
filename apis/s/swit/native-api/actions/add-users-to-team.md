# Add Users To Team with Swit

Adds users to a team in Swit.

## Endpoint

- **Method:** `POST`
- **Path:** `team.user.add`
- **Base URL:** `https://openapi.swit.io`
- **Official documentation:** [Add Users To Team](https://tech-support.swit.io/books/swit-java-development-guide/page/05f97)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Target team ID. |
| `user_ids[]` | body | `array<string>` | yes | List of user IDs to add to the team. Send multiple values as a array. |
