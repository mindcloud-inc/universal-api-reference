# Remove Team Member by Email or IdP ID with Filestage

Deletes a Filestage team member by email or IdP ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/team/members`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Remove Team Member by Email or IdP ID](https://developers.filestage.io/docs/api/oadv4f9asb1oe-remove-team-member-by-email-or-idpid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Email |
| `idpId` | query | `string` | no | The user id in your identity provider |
| `forceRemove` | query | `boolean` | no | When set to true, the forceRemove flag ensures the forceful removal of users with Webhooks and API keys. If you attempt to remove a user with Webhooks or API keys without setting the forceRemove flag to true, a 403 Forbidden error will be thrown. |
| `deleteFromReviews` | query | `boolean` | no | When set to true, the member will be removed from the review groups of all projects in this team. If false (default), the member will retain access to reviews they were already part of, even after being removed from the team. |
