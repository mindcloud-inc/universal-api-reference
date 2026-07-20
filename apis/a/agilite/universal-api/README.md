# Agilite: Universal API

Agilit-e centralizes business logic and processes as API-accessible microservices, including keywords, BPM workflows, roles, templates, connectors, data mapping, numbering, files, and utility services.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agilite/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://agilite.io
- **Vendor API docs:** https://docs.agilite.io/docs/api-server-fundamentals

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Active BPM Steps](actions/get-active-bpm-steps.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/get-active-bpm-steps?connectionId=$CONNECTION_ID&processKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Active Bpm Step

| Action | Method | Description |
| --- | --- | --- |
| [Get Active BPM Steps](actions/get-active-bpm-steps.md) | GET | Retrieves active BPM steps from Agilite by process key. |

### Active Bpm User

| Action | Method | Description |
| --- | --- | --- |
| [Get Active BPM Users](actions/get-active-bpm-users.md) | GET | Retrieves active BPM users from Agilite by process key. |

### Assigned Bpm Role

| Action | Method | Description |
| --- | --- | --- |
| [Get Assigned BPM Roles](actions/get-assigned-bpm-roles.md) | GET | Retrieves assigned BPM roles from Agilite for a BPM record. |

### Bpm Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get BPM Profile By Key](actions/get-bpm-profile-by-key.md) | GET | Retrieves BPM profiles from Agilite by profile key. |

### Bpm Record

| Action | Method | Description |
| --- | --- | --- |
| [Register BPM Record](actions/register-bpm-record.md) | POST | Registers a new BPM record in Agilite. |

### Bpm Record State

| Action | Method | Description |
| --- | --- | --- |
| [Get BPM Record State](actions/get-bpm-record-state.md) | GET | Retrieves a BPM record state from Agilite. |

### Bpm Role Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Assign BPM Role](actions/assign-bpm-role.md) | PUT | Assigns a role to a BPM record in Agilite. |

### Bpm Step Execution

| Action | Method | Description |
| --- | --- | --- |
| [Execute BPM Step](actions/execute-bpm-step.md) | PUT | Executes a BPM record in Agilite. |

### Connector Result

| Action | Method | Description |
| --- | --- | --- |
| [Execute Connector Route](actions/execute-connector-route.md) | POST | Executes a connector route in Agilite by profile and route key. |

### Data Mapping Result

| Action | Method | Description |
| --- | --- | --- |
| [Execute Data Mapping](actions/execute-data-mapping.md) | POST | Executes a data mapping profile in Agilite by profile key. |

### Generated Number

| Action | Method | Description |
| --- | --- | --- |
| [Generate Number](actions/generate-number.md) | POST | Generates a unique number in Agilite by profile key. |

### Keyword Label

| Action | Method | Description |
| --- | --- | --- |
| [Get Keyword Label By Value](actions/get-keyword-label-by-value.md) | GET | Retrieves a keyword label from Agilite by profile and value key. |

### Keyword Profile

| Action | Method | Description |
| --- | --- | --- |
| [List Keyword Profiles](actions/list-keyword-profiles.md) | GET | Retrieves all keyword profiles from Agilite. |

### Keyword Profile Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Keyword Profile Keys By Group](actions/get-keyword-profile-keys-by-group.md) | GET | Retrieves keyword profile keys from Agilite by group. |

### Keyword Value

| Action | Method | Description |
| --- | --- | --- |
| [Get Keyword Value By Label](actions/get-keyword-value-by-label.md) | GET | Retrieves a keyword value from Agilite by profile and label key. |
| [Get Keyword Values By Profile Key](actions/get-keyword-values-by-profile-key.md) | GET | Retrieves keyword values from Agilite by profile key. |

### Numbering Profile

| Action | Method | Description |
| --- | --- | --- |
| [List Numbering Profiles](actions/list-numbering-profiles.md) | GET | Retrieves all numbering profiles from Agilite. |

### Responsible Bpm Role

| Action | Method | Description |
| --- | --- | --- |
| [Get Responsible BPM Roles](actions/get-responsible-bpm-roles.md) | GET | Retrieves responsible BPM roles from Agilite for a BPM stub. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Get Role](actions/get-role.md) | GET | Retrieves responsible users from Agilite by role and conditional level. |

### Template Profile

| Action | Method | Description |
| --- | --- | --- |
| [List Template Profiles](actions/list-template-profiles.md) | GET | Retrieves all template profiles from Agilite. |

### Template Result

| Action | Method | Description |
| --- | --- | --- |
| [Execute Template](actions/execute-template.md) | POST | Executes a template in Agilite by profile key. |

### Tier Structure

| Action | Method | Description |
| --- | --- | --- |
| [Get Tier Structure By Key](actions/get-tier-structure-by-key.md) | GET | Retrieves tier structure profiles from Agilite by tier keys. |
| [List Tier Structures](actions/list-tier-structures.md) | GET | Retrieves all tier structure profiles from Agilite. |

### Uuid

| Action | Method | Description |
| --- | --- | --- |
| [Generate UUID](actions/generate-uuid.md) | POST | Generates a new UUID in Agilite. |

