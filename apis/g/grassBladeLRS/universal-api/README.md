# <img src="https://images.mindcloud.co/apps/icons/grass-blade-lrs_1775491932754.png" alt="GrassBlade LRS logo" width="28" height="28"> GrassBlade LRS: Universal API

Query learning records and xAPI statements

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/grassBladeLRS/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nextsoftwaresolutions.com/grassblade-lrs/
- **Vendor API docs:** https://github.com/adlnet/xAPI-Spec/tree/xAPI-1.0.3

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get About](actions/get-about.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/get-about?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### About

| Action | Method | Description |
| --- | --- | --- |
| [Get About](actions/get-about.md) | GET | Retrieves LRS about information from GrassBlade LRS. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity By ID](actions/get-activity-by-id.md) | GET | Retrieves an activity by ID from GrassBlade LRS. |

### Activity Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity Profile](actions/create-activity-profile.md) | POST | Stores or updates an activity profile in GrassBlade LRS. |
| [Delete Activity Profile](actions/delete-activity-profile.md) | DELETE | Deletes an activity profile from GrassBlade LRS. |
| [Get Activity Profile](actions/get-activity-profile.md) | GET | Retrieves an activity profile from GrassBlade LRS. |
| [Replace Activity Profile](actions/replace-activity-profile.md) | PUT | Replaces an activity profile in GrassBlade LRS. |

### Activity Profile Id

| Action | Method | Description |
| --- | --- | --- |
| [List Activity Profile IDs](actions/list-activity-profile-ids.md) | GET | Retrieves activity profile IDs from GrassBlade LRS. |
| [List Activity Profile IDs Since](actions/list-activity-profile-ids-since.md) | GET | Retrieves activity profile IDs from GrassBlade LRS since a timestamp. |

### Agent Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent Profile](actions/create-agent-profile.md) | POST | Stores or updates an agent profile in GrassBlade LRS. |
| [Delete Agent Profile](actions/delete-agent-profile.md) | DELETE | Deletes an agent profile from GrassBlade LRS. |
| [Get Agent Profile](actions/get-agent-profile.md) | GET | Retrieves an agent profile from GrassBlade LRS. |
| [Replace Agent Profile](actions/replace-agent-profile.md) | PUT | Replaces an agent profile in GrassBlade LRS. |

### Agent Profile Id

| Action | Method | Description |
| --- | --- | --- |
| [List Agent Profile IDs](actions/list-agent-profile-ids.md) | GET | Retrieves agent profile IDs from GrassBlade LRS. |
| [List Agent Profile IDs Since](actions/list-agent-profile-ids-since.md) | GET | Retrieves agent profile IDs from GrassBlade LRS since a timestamp. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Person By Agent](actions/get-person-by-agent.md) | GET | Retrieves person details from GrassBlade LRS by agent. |

### State Document

| Action | Method | Description |
| --- | --- | --- |
| [Create State Document](actions/create-state-document.md) | POST | Stores or updates a state document in GrassBlade LRS. |
| [Delete All State For Context](actions/delete-all-state-for-context.md) | DELETE | Deletes all state documents for a context in GrassBlade LRS. |
| [Delete State Document](actions/delete-state-document.md) | DELETE | Deletes a state document from GrassBlade LRS. |
| [Get State Document](actions/get-state-document.md) | GET | Retrieves a state document from GrassBlade LRS. |
| [Replace State Document](actions/replace-state-document.md) | PUT | Replaces a state document in GrassBlade LRS. |

### State Id

| Action | Method | Description |
| --- | --- | --- |
| [List State IDs](actions/list-state-ids.md) | GET | Retrieves state document IDs from GrassBlade LRS. |
| [List State IDs Since](actions/list-state-ids-since.md) | GET | Retrieves state document IDs from GrassBlade LRS since a timestamp. |

### Statement

| Action | Method | Description |
| --- | --- | --- |
| [Create Statement](actions/create-statement.md) | POST | Stores a statement in GrassBlade LRS. |
| [Create Statement Batch](actions/create-statement-batch.md) | POST | Stores a batch of statements in GrassBlade LRS. |
| [Create Statement By ID](actions/create-statement-by-id.md) | PUT | Stores a statement by ID in GrassBlade LRS. |
| [Get Statement By ID](actions/get-statement-by-id.md) | GET | Retrieves a statement by ID from GrassBlade LRS. |
| [Get Voided Statement](actions/get-voided-statement.md) | GET | Retrieves a voided statement from GrassBlade LRS. |
| [List Statements](actions/list-statements.md) | GET | Retrieves statements from GrassBlade LRS. |
| [Search Statements By Activity](actions/search-statements-by-activity.md) | GET | Finds statements in GrassBlade LRS by activity. |
| [Search Statements By Agent](actions/search-statements-by-agent.md) | GET | Finds statements in GrassBlade LRS by agent. |
| [Search Statements By Registration](actions/search-statements-by-registration.md) | GET | Finds statements in GrassBlade LRS by registration. |
| [Search Statements By Time Window](actions/search-statements-by-time-window.md) | GET | Finds statements in GrassBlade LRS by time window. |
| [Search Statements By Verb](actions/search-statements-by-verb.md) | GET | Finds statements in GrassBlade LRS by verb. |

