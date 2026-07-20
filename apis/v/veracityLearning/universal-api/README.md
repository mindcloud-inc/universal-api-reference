# <img src="https://images.mindcloud.co/apps/icons/veracity-learning_1775824401718.png" alt="Veracity Learning logo" width="28" height="28"> Veracity Learning: Universal API

Manage xAPI statements, profiles, and activity state

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/veracityLearning/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lrs.io
- **Vendor API docs:** https://oliver.enterprise.lrs.io/docs/manual/basics/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Statements](actions/list-statements.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-statements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | GET | Retrieves an activity from Veracity Learning. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Activity Profile Document](actions/delete-activity-profile-document.md) | DELETE | Deletes an activity profile document from Veracity Learning. |
| [Delete Agent Profile Document](actions/delete-agent-profile-document.md) | DELETE | Deletes an agent profile document from Veracity Learning. |
| [Delete All State Documents](actions/delete-all-state-documents.md) | DELETE | Deletes all state documents from Veracity Learning. |
| [Delete State Document](actions/delete-state-document.md) | DELETE | Deletes a state document from Veracity Learning. |
| [Get Activity Profile Document](actions/get-activity-profile-document.md) | GET | Retrieves an activity profile document from Veracity Learning. |
| [Get Agent Profile Document](actions/get-agent-profile-document.md) | GET | Retrieves an agent profile document from Veracity Learning. |
| [Get State Document](actions/get-state-document.md) | GET | Retrieves a state document from Veracity Learning. |
| [List Activity Profile IDs](actions/list-activity-profile-ids.md) | GET | Lists activity profile IDs from Veracity Learning. |
| [List Agent Profile IDs](actions/list-agent-profile-ids.md) | GET | Lists agent profile IDs from Veracity Learning. |
| [List State IDs](actions/list-state-ids.md) | GET | Lists state document IDs from Veracity Learning. |
| [Merge Activity Profile Document](actions/merge-activity-profile-document.md) | PUT | Updates an activity profile document in Veracity Learning by merging content. |
| [Merge Agent Profile Document](actions/merge-agent-profile-document.md) | PUT | Updates an agent profile document in Veracity Learning by merging content. |
| [Merge State Document](actions/merge-state-document.md) | PUT | Updates a state document in Veracity Learning by merging content. |
| [Put Activity Profile Document](actions/put-activity-profile-document.md) | PUT | Updates an activity profile document in Veracity Learning. |
| [Put Agent Profile Document](actions/put-agent-profile-document.md) | PUT | Updates an agent profile document in Veracity Learning. |
| [Put State Document](actions/put-state-document.md) | PUT | Updates a state document in Veracity Learning. |

### Lrsinfo

| Action | Method | Description |
| --- | --- | --- |
| [Get LRS About](actions/get-lrs-about.md) | GET | Retrieves LRS information from Veracity Learning. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent](actions/get-agent.md) | GET | Retrieves a Person Object for an agent from Veracity Learning. |

### Statement

| Action | Method | Description |
| --- | --- | --- |
| [Create Statements](actions/create-statements.md) | POST | Creates one or more statements in Veracity Learning. |
| [Get More Statements](actions/get-more-statements.md) | GET | Retrieves more statements from Veracity Learning. |
| [Get Statement](actions/get-statement.md) | GET | Retrieves a statement from Veracity Learning by statement ID. |
| [Get Voided Statement](actions/get-voided-statement.md) | GET | Retrieves a voided statement from Veracity Learning by statement ID. |
| [List Statements](actions/list-statements.md) | GET | Retrieves statements from Veracity Learning. |
| [Put Statement](actions/put-statement.md) | POST | Creates a single statement in Veracity Learning using a statement ID. |

