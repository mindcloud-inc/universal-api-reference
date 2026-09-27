# Endorse a skill on a LinkedIn profile with ConnectSafely

Endorse a specific skill on a LinkedIn profile, or randomly select and endorse an unendorsed skill. When random=true, the endpoint fetches all skills on the profile, filters out already-endorsed ones, and randomly endorses one.

## Endpoint

- **Method:** `POST`
- **Path:** `/endorse-skill`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Endorse a skill on a LinkedIn profile](https://connectsafely.ai/docs/api/linkedin-profiles/post-endorse-skill-endorse-skill)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `profileId` | body | `string` | yes | LinkedIn profile vanity URL slug (the part after linkedin.com/in/, e.g., "john-doe-123") |
| `skillId` | body | `string` | no | Specific skill ID to endorse (from skills list) |
| `random` | body | `boolean` | no | If true, randomly select an unendorsed skill to endorse Default: `False`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` | Whether the endorsement was successful |
| `profileId` | `string` | The profile vanity URL slug |
| `memberId` | `string` | The profile member ID |
| `skillId` | `string` | The ID of the endorsed skill |
| `skillName` | `string` | Name of the endorsed skill (only when random=true) |
| `random` | `boolean` | Whether a random skill was selected |
| `message` | `string` | Success message |

### Example response

```json
{
  "success": true,
  "profileId": "john-doe-123",
  "memberId": "ACoAAABpGQcMBI08myTal7qDJ5zb9lJiM24nFjJI",
  "skillId": "5",
  "skillName": "JavaScript",
  "random": true,
  "message": "Successfully endorsed skill: JavaScript"
}
```

## Error status codes

`400`, `404`. Bodies follow the shared `{ success, code, message }` error shape.
