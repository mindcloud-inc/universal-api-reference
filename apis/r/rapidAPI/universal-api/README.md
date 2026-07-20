# <img src="https://images.mindcloud.co/apps/icons/rapid-apirestplatform-api_1775591504204.png" alt="RapidAPI logo" width="28" height="28"> RapidAPI: Universal API

RapidAPI Enterprise Hub REST Platform API draft wrapper for the publicly documented app, API, user, organization, and team management REST example surface.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rapidAPI/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rapidapi.com
- **Vendor API docs:** https://docs.rapidapi.com/docs/platform-api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Apps](actions/list-apps.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rapidAPI/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Api

| Action | Method | Description |
| --- | --- | --- |
| [List APIs](actions/list-apis.md) | GET | Retrieves APIs from RapidAPI. |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [List App Keys](actions/list-app-keys.md) | GET | Retrieves app keys from RapidAPI. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get App](actions/get-app.md) | GET | Retrieves app details from RapidAPI. |
| [List Apps](actions/list-apps.md) | GET | Retrieves apps from RapidAPI. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from RapidAPI. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Entity Roles](actions/list-entity-roles.md) | GET | Retrieves roles for an entity in RapidAPI. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Teams](actions/list-organization-teams.md) | GET | Retrieves teams for a RapidAPI organization. |
| [List User Teams](actions/list-user-teams.md) | GET | Retrieves teams for a RapidAPI user. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from RapidAPI. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in RapidAPI. |

