# <img src="https://images.mindcloud.co/apps/icons/icon_1776962205810.png" alt="BASIC logo" width="28" height="28"> BASIC: Universal API

BASIC: Manage projects, teams, users, and schemas

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bASIC/latest
- **Category:** IT Operations / Database
- **Actions:** 64
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://basic.tech
- **Vendor API docs:** https://docs.basic.tech/basic-restapi/basic-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get all admin projects of developer](actions/list-admin-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/list-admin-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (64)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get auth token](actions/get-auth-token.md) | POST | Creates OAuth tokens in BASIC. |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Create new API key](actions/create-new-api-key.md) | POST | Creates a new API key in BASIC. |
| [Delete API key](actions/delete-api-key.md) | DELETE | Deletes an existing API key from BASIC. |
| [Get all keys for a project](actions/get-all-keys-for-a-project.md) | GET | Retrieves project API keys from BASIC. |
| [Get specific API key](actions/get-specific-api-key.md) | GET | Retrieves a specific API key from BASIC. |
| [Regenerate API key](actions/regenerate-api-key.md) | PUT | Regenerates an API key in BASIC. |
| [Update API key](actions/update-api-key.md) | PUT | Updates an existing API key in BASIC. |
| [Verify API key](actions/verify-api-key.md) | GET | Verifies an API key in BASIC. |

### Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [OpenID Connect Discovery Document](actions/open-id-connect-discovery-document.md) | GET | Retrieves the OpenID Connect discovery document from BASIC. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create item](actions/create-item.md) | POST | Creates a new item in a BASIC table. |
| [Delete an item](actions/delete-an-item.md) | DELETE | Deletes an existing item from a BASIC table. |
| [Get all items in a table](actions/get-all-items-in-a-table.md) | GET | Retrieves all items from a BASIC table. |
| [Get specific item in a table](actions/get-specific-item-in-a-table.md) | GET | Retrieves an item from a BASIC table. |
| [Replace an item](actions/replace-an-item.md) | PUT | Replaces an existing item in a BASIC table. |
| [Update an item](actions/update-an-item.md) | PUT | Updates an existing item in a BASIC table. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Compare two schemas](actions/compare-two-schemas.md) | GET | Compares two schemas in BASIC. |
| [Verify update schema](actions/verify-update-schema.md) | GET | Verifies an update schema in BASIC. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Check project slug availability](actions/check-project-slug-availability.md) | GET | Checks project slug availability in BASIC. |
| [Create a new project](actions/create-a-new-project.md) | POST | Creates a new project in BASIC. |
| [Delete a project](actions/delete-a-project.md) | DELETE | Deletes an existing project from BASIC. |
| [Delete project background image](actions/delete-project-background-image.md) | DELETE | Deletes a project background image from BASIC. |
| [Delete project icon](actions/delete-project-icon.md) | DELETE | Deletes a project icon from BASIC. |
| [Delete specific settings values](actions/delete-specific-settings-values.md) | DELETE | Deletes specific project setting values from BASIC. |
| [Generate or update suggested schema using AI](actions/generate-or-update-suggested-schema-using-ai.md) | PUT | Generates or updates a suggested schema with AI in BASIC. |
| [Get client metadata document](actions/get-client-metadata-document.md) | GET | Retrieves a client metadata document from BASIC. |
| [Get project details](actions/get-project-details.md) | GET | Retrieves project details from BASIC. |
| [Get project DID document](actions/get-project-did-document.md) | GET | Retrieves a project DID document from BASIC. |
| [Get project images](actions/get-project-images.md) | GET | Retrieves project icon and background images from BASIC. |
| [Get project public profile](actions/get-project-public-profile.md) | GET | Retrieves a project public profile from BASIC. |
| [Get project schema](actions/get-project-schema.md) | GET | Retrieves a project schema from BASIC. |
| [Get project settings](actions/get-project-settings.md) | GET | Retrieves project settings from BASIC. |
| [Get all admin projects of developer](actions/list-admin-projects.md) | GET | Retrieves admin projects for the current developer in BASIC. |
| [Merge and update project schema](actions/merge-and-update-project-schema.md) | PUT | Merges and updates a project schema in BASIC. |
| [Update project details](actions/update-project-details.md) | PUT | Updates existing project details in BASIC. |
| [Update project schema](actions/update-project-schema.md) | PUT | Updates a project schema in BASIC. |
| [Update project settings](actions/update-project-settings.md) | PUT | Updates existing project settings in BASIC. |
| [Upload project background image](actions/upload-project-background-image.md) | PUT | Uploads a project background image to BASIC. |
| [Upload project icon](actions/upload-project-icon.md) | PUT | Uploads a project icon to BASIC. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Convert text to URL-friendly slug](actions/convert-text-to-url-friendly-slug.md) | GET | Converts text to a URL-friendly slug in BASIC. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [JSON Web Key Set](actions/j-son-web-key-set.md) | GET | Retrieves the JSON Web Key Set from BASIC. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Redirect to sign in](actions/redirect-to-sign-in.md) | GET | Retrieves an OAuth sign-in redirect from BASIC. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Check auth endpoint status](actions/check-auth-endpoint-status.md) | GET | Checks the auth endpoint status in BASIC. |
| [Check Root Endpoint Status](actions/check-root-endpoint-status.md) | GET | Checks the root endpoint status in BASIC. |
| [Check Utils Endpoint Status](actions/check-utils-endpoint-status.md) | GET | Checks the utils endpoint status in BASIC. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Accept a team invite](actions/accept-a-team-invite.md) | POST | Accepts a team invite in BASIC. |
| [Check team slug availability](actions/check-team-slug-availability.md) | GET | Checks team slug availability in BASIC. |
| [Create a new team](actions/create-a-new-team.md) | POST | Creates a new team in BASIC. |
| [Create a team invite](actions/create-a-team-invite.md) | POST | Creates a team invite in BASIC. |
| [Delete a team](actions/delete-a-team.md) | DELETE | Deletes an existing team from BASIC. |
| [Delete a team invite](actions/delete-a-team-invite.md) | DELETE | Deletes a team invite from BASIC. |
| [Delete a team member](actions/delete-a-team-member.md) | DELETE | Deletes a team member from BASIC. |
| [Get team by ID](actions/get-team-by-id.md) | GET | Retrieves a team by ID from BASIC. |
| [Get team invites](actions/get-team-invites.md) | GET | Retrieves team invites from BASIC. |
| [Get team members](actions/get-team-members.md) | GET | Retrieves team members from BASIC. |
| [Get user teams](actions/get-user-teams.md) | GET | Retrieves user teams from BASIC. |
| [Update a team](actions/update-a-team.md) | PUT | Updates an existing team in BASIC. |
| [Update a team member](actions/update-a-team-member.md) | PUT | Updates an existing team member in BASIC. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Delete a user from the project](actions/delete-a-user-from-the-project.md) | DELETE | Deletes a user from a BASIC project. |
| [Get all users in project](actions/get-all-users-in-project.md) | GET | Retrieves project users from BASIC. |
| [Get project activity stats](actions/get-project-activity-stats.md) | GET | Retrieves project activity stats from BASIC. |
| [Get user details](actions/get-user-details.md) | GET | Retrieves user details from BASIC. |
| [Get user info](actions/get-user-info.md) | GET | Retrieves user information from BASIC. |
| [Report a user connection to this project](actions/report-a-user-connection-to-this-project.md) | POST | Records a user connection in a BASIC project. |
| [Update user metadata](actions/update-user-metadata.md) | PUT | Updates existing user metadata in BASIC. |

