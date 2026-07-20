# <img src="https://images.mindcloud.co/apps/icons/sprinklr_1775829489069.png" alt="Sprinklr logo" width="28" height="28"> Sprinklr: Universal API

Sprinklr is an AI-native customer experience platform. This wrapper provides OAuth-authenticated access to Sprinklr API 2.0 resources including search, standard entities, custom entities, accounts, tasks, cases, profiles, messages, and comments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sprinklr/latest
- **Category:** Support / Contact Center
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sprinklr.com/
- **Vendor API docs:** https://dev.sprinklr.com/api2-0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Custom Entity Definitions](actions/list-custom-entity-definitions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/list-custom-entity-definitions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Sprinklr. |

### Cases

| Action | Method | Description |
| --- | --- | --- |
| [Create Case](actions/create-case.md) | POST | Creates a case in Sprinklr. |
| [Get Case](actions/get-case.md) | GET | Retrieves a case from Sprinklr. |
| [Update Case](actions/update-case.md) | PUT | Updates an existing case in Sprinklr. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | POST | Creates a comment in Sprinklr. |

### Custom Entity

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Entity](actions/create-custom-entity.md) | POST | Creates a custom entity in Sprinklr. |
| [Delete Custom Entity](actions/delete-custom-entity.md) | DELETE | Deletes an existing custom entity from Sprinklr. |
| [Get Custom Entity](actions/get-custom-entity.md) | GET | Retrieves a custom entity from Sprinklr. |
| [Patch Custom Entity](actions/patch-custom-entity.md) | PUT | Updates part of a custom entity in Sprinklr. |
| [Update Custom Entity](actions/update-custom-entity.md) | PUT | Updates an existing custom entity in Sprinklr. |
| [Upsert Custom Entity](actions/upsert-custom-entity.md) | PUT | Updates or creates a custom entity in Sprinklr. |

### Custom Entity Definition

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Entity Definitions](actions/list-custom-entity-definitions.md) | GET | Retrieves custom entity definitions from Sprinklr. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Standard Entity Field](actions/get-standard-entity-field.md) | GET | Retrieves a standard entity field from Sprinklr. |
| [List Custom Entity Fields](actions/list-custom-entity-fields.md) | GET | Retrieves custom entity fields from Sprinklr. |
| [List Standard Entity Fields](actions/list-standard-entity-fields.md) | GET | Retrieves standard entity fields from Sprinklr. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Sprinklr. |
| [List Case Messages](actions/list-case-messages.md) | GET | Retrieves case messages from Sprinklr. |
| [Perform Message Action](actions/perform-message-action.md) | PUT | Updates a message in Sprinklr by performing an action. |

### Participant

| Action | Method | Description |
| --- | --- | --- |
| [Create Participant](actions/create-participant.md) | POST | Creates a participant in Sprinklr. |
| [Get Participant](actions/get-participant.md) | GET | Retrieves a participant from Sprinklr. |
| [List Account Participants](actions/list-account-participants.md) | GET | Retrieves account participants from Sprinklr. |
| [Update Account Participant](actions/update-account-participant.md) | PUT | Updates an existing account participant in Sprinklr. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Results Page](actions/get-search-results-page.md) | GET | Retrieves a search results page from Sprinklr. |
| [Search Entities](actions/search-entities.md) | GET | Finds entities in Sprinklr by search criteria. |

### Standard Entity

| Action | Method | Description |
| --- | --- | --- |
| [Create Standard Entity](actions/create-standard-entity.md) | POST | Creates a standard entity in Sprinklr. |
| [Delete Standard Entity](actions/delete-standard-entity.md) | DELETE | Deletes an existing standard entity from Sprinklr. |
| [Get Standard Entity](actions/get-standard-entity.md) | GET | Retrieves a standard entity from Sprinklr. |
| [Get Standard Entity By Primary Key](actions/get-standard-entity-by-primary-key.md) | GET | Retrieves a standard entity from Sprinklr by primary key. |
| [Patch Standard Entity](actions/patch-standard-entity.md) | PUT | Updates part of a standard entity in Sprinklr. |
| [Search Standard Entities By Primary Key Prefix](actions/search-standard-entities-by-primary-key-prefix.md) | GET | Finds standard entities in Sprinklr by primary key prefix. |
| [Update Standard Entity](actions/update-standard-entity.md) | PUT | Updates an existing standard entity in Sprinklr. |
| [Upsert Standard Entity](actions/upsert-standard-entity.md) | PUT | Updates or creates a standard entity in Sprinklr. |
| [Upsert Standard Entity By Primary Key](actions/upsert-standard-entity-by-primary-key.md) | PUT | Updates or creates a standard entity in Sprinklr by primary key. |

### Standard Entity Definition

| Action | Method | Description |
| --- | --- | --- |
| [Get Standard Entity Definition](actions/get-standard-entity-definition.md) | GET | Retrieves a standard entity definition from Sprinklr. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a task in Sprinklr. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Sprinklr. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Sprinklr. |
| [Get Tasks](actions/get-tasks.md) | GET | Retrieves tasks from Sprinklr. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Sprinklr. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Search Profiles](actions/search-profiles.md) | GET | Finds profiles in Sprinklr by search criteria. |

