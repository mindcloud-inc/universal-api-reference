# Remove Team Member by Member ID with Filestage

Deletes a Filestage team member by member ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/team/members/{memberId}`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Remove Team Member by Member ID](https://developers.filestage.io/docs/api/3h6t5yy5kd534-remove-team-member-by-memberid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `forceRemove` | query | `boolean` | no | When set to true, the forceRemove flag ensures the forceful removal of users with Webhooks and API keys. If you attempt to remove a user with Webhooks or API keys without setting the forceRemove flag to true, a 403 Forbidden error will be thrown. |
| `deleteFromReviews` | query | `boolean` | no | When set to true, the member will be removed from the review groups of all projects in this team. If false (default), the member will retain access to reviews they were already part of, even after being removed from the team. |
| `memberId` | path | `string` | yes | Filestage user id |
