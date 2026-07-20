# Agilite: Native API Reference

A consolidated summary of Agilite's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.agilite.io/docs/api-server-fundamentals
- **API base URL:** `https://api.agilite.io`

## Authentication

### Agilite API Key

Authenticate requests to the Agilit-e API Server with an API key in the `api-key` request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.agilite.io/docs/api-server-fundamentals)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign BPM Role](actions/assign-bpm-role.md) | `GET /bpm/assignRole` | [docs](https://docs.agilite.io/reference/assignrole) |
| [Execute BPM Step](actions/execute-bpm-step.md) | `POST /bpm/execute` | [docs](https://docs.agilite.io/reference/execute) |
| [Execute Connector Route](actions/execute-connector-route.md) | `POST /connectors/execute` | [docs](https://docs.agilite.io/reference/execute-2) |
| [Execute Data Mapping](actions/execute-data-mapping.md) | `POST /datamappings/execute` | [docs](https://docs.agilite.io/reference/execute-1) |
| [Execute Template](actions/execute-template.md) | `POST /templates/execute` | [docs](https://docs.agilite.io/reference/execute-3) |
| [Generate Number](actions/generate-number.md) | `POST /numbering/generate` | [docs](https://docs.agilite.io/reference/generate) |
| [Generate UUID](actions/generate-uuid.md) | `GET /utils/generateUUID` | [docs](https://docs.agilite.io/reference/generateuuid) |
| [Get Active BPM Steps](actions/get-active-bpm-steps.md) | `GET /bpm/getActiveSteps` | [docs](https://docs.agilite.io/reference/getactivesteps) |
| [Get Active BPM Users](actions/get-active-bpm-users.md) | `GET /bpm/getActiveUsers` | [docs](https://docs.agilite.io/reference/getactiveusers) |
| [Get Assigned BPM Roles](actions/get-assigned-bpm-roles.md) | `GET /bpm/getAssignedRoles` | [docs](https://docs.agilite.io/reference/getassignedroles) |
| [Get BPM Profile By Key](actions/get-bpm-profile-by-key.md) | `GET /bpm/getByProfileKey` | [docs](https://docs.agilite.io/reference/getbyprofilekey-1) |
| [Get BPM Record State](actions/get-bpm-record-state.md) | `GET /bpm/getRecordState` | [docs](https://docs.agilite.io/reference/getrecordstate) |
| [Get Keyword Label By Value](actions/get-keyword-label-by-value.md) | `GET /keywords/getLabelByValue` | [docs](https://docs.agilite.io/reference/getlabelbyvalue) |
| [Get Keyword Profile Keys By Group](actions/get-keyword-profile-keys-by-group.md) | `GET /keywords/getProfileKeysByGroup` | [docs](https://docs.agilite.io/reference/getprofilekeysbygroup) |
| [Get Keyword Value By Label](actions/get-keyword-value-by-label.md) | `GET /keywords/getValueByLabel` | [docs](https://docs.agilite.io/reference/getvaluebylabel) |
| [Get Keyword Values By Profile Key](actions/get-keyword-values-by-profile-key.md) | `GET /keywords/getValuesByProfileKey` | [docs](https://docs.agilite.io/reference/getbyprofilekey) |
| [Get Responsible BPM Roles](actions/get-responsible-bpm-roles.md) | `GET /bpm/getResponsibleRoles` | [docs](https://docs.agilite.io/reference/getresponsibleroles) |
| [Get Role](actions/get-role.md) | `POST /roles/getRole` | [docs](https://docs.agilite.io/reference/getrole) |
| [Get Tier Structure By Key](actions/get-tier-structure-by-key.md) | `GET /tierstructures/getTierByKey` | [docs](https://docs.agilite.io/reference/gettierbykey) |
| [List Keyword Profiles](actions/list-keyword-profiles.md) | `GET /keywords/data` | [docs](https://docs.agilite.io/reference/data-1) |
| [List Numbering Profiles](actions/list-numbering-profiles.md) | `GET /numbering/data` | [docs](https://docs.agilite.io/reference/data-2) |
| [List Template Profiles](actions/list-template-profiles.md) | `GET /templates/data` | [docs](https://docs.agilite.io/reference/data-4) |
| [List Tier Structures](actions/list-tier-structures.md) | `GET /tierstructures/data` | [docs](https://docs.agilite.io/reference/data-3) |
| [Register BPM Record](actions/register-bpm-record.md) | `GET /bpm/registerBPMRecord` | [docs](https://docs.agilite.io/reference/registerbpmrecord) |
