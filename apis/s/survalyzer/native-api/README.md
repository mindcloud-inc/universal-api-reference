# Survalyzer: Native API Reference

A consolidated summary of Survalyzer's API configuration and 43 documented operations, with links to official documentation.

- **Official docs:** https://developer.survalyzer.com/knowledge-base/public-api-eu/
- **OpenAPI specification:** https://learn.microsoft.com/en-us/connectors/survalyzereu/
- **API base URL:** `https://api.survalyzer-eu.app`

## Authentication

### Bearer Token

Store a Survalyzer EU bearer token obtained from the OAuth password-grant token endpoint.

### Credentials

- **Access Token:** `accessToken` · optional · Bearer access token returned by the Survalyzer EU OAuth token endpoint.

Send these headers with each API request:

```http
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://developer.survalyzer.com/knowledge-base/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (43 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create And Invite Members](actions/create-and-invite-members.md) | `POST /publicapi/Distribute/v3/CreateAndInviteMembers` | [docs](https://developer.survalyzer.com/knowledge-base/code-examples/) |
| [Create Artifact](actions/create-artifact.md) | `POST /publicapi/Common/v3/CreateArtifact` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Create Members](actions/create-members.md) | `POST /publicapi/Panel/v3/CreateMembers` | [docs](https://developer.survalyzer.com/knowledge-base/code-examples/) |
| [Create Panel](actions/create-panel.md) | `POST /publicapi/Panel/v3/CreatePanel` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Create Survey](actions/create-survey.md) | `POST /publicapi/Survey/v3/CreateSurvey` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Create WebHook](actions/create-web-hook.md) | `POST /publicapi/WebHook/v3/CreateWebHook` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Delete Artifact](actions/delete-artifact.md) | `POST /publicapi/Common/v3/DeleteArtifact` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Delete Distributor](actions/delete-distributor.md) | `POST /publicapi/Distribute/v3/DeleteDistributor` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Delete Interview](actions/delete-interview.md) | `POST /publicapi/Interview/v3/DeleteInterview` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Delete Members](actions/delete-members.md) | `POST /publicapi/Panel/v3/DeleteMembers` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Delete Panel](actions/delete-panel.md) | `POST /publicapi/Panel/v3/DeletePanel` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Delete Sampling Project](actions/delete-sampling-project.md) | `POST /publicapi/Distribute/v3/DeleteSamplingProject` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Delete Survey](actions/delete-survey.md) | `POST /publicapi/Survey/v3/DeleteSurvey` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Delete WebHook](actions/delete-web-hook.md) | `POST /publicapi/WebHook/v3/DeleteWebHook` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Execute Workflow Transition](actions/execute-workflow-transition.md) | `POST /publicapi/Workflow/v3/ExecuteWorkflowTransition` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Get Credit Balance](actions/get-credit-balance.md) | `POST /publicapi/Incentive/v3/ReadCreditBalance` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Get Interview](actions/get-interview.md) | `POST /publicapi/Interview/v3/ReadInterview` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Get Panel](actions/get-panel.md) | `POST /publicapi/Panel/v3/ReadPanel` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Get Sampling Project](actions/get-sampling-project.md) | `POST /publicapi/Distribute/v3/ReadSamplingProject` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Get Survey](actions/get-survey.md) | `POST /publicapi/Survey/v3/ReadSurvey` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Invite Members](actions/invite-members.md) | `POST /publicapi/Distribute/v3/InviteMembers` | [docs](https://developer.survalyzer.com/knowledge-base/code-examples/) |
| [List Artifacts](actions/list-artifacts.md) | `POST /publicapi/Common/v3/ReadArtifactList` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List Bounces](actions/list-bounces.md) | `POST /publicapi/Distribute/v3/ReadBounceList` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List Distributors](actions/list-distributors.md) | `POST /publicapi/Distribute/v3/ReadDistributorList` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List Incentive Transactions](actions/list-incentive-transactions.md) | `POST /publicapi/Incentive/v3/ReadIncentiveTransactionList` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List Incentives](actions/list-incentives.md) | `POST /publicapi/Incentive/v3/ReadIncentiveList` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List Interviews](actions/list-interviews.md) | `POST /publicapi/Interview/v3/ReadInterviewList` | [docs](https://developer.survalyzer.com/knowledge-base/code-examples/) |
| [List Interviews Compact](actions/list-interviews-compact.md) | `POST /publicapi/Interview/v3/ReadInterviewListCompact` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List Members](actions/list-members.md) | `POST /publicapi/Panel/v3/ReadMemberList` | [docs](https://developer.survalyzer.com/knowledge-base/code-examples/) |
| [List Message Templates](actions/list-message-templates.md) | `POST /publicapi/Distribute/v3/ReadMessageTemplateList` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List Opt-Outs](actions/list-opt-outs.md) | `POST /publicapi/Distribute/v3/ReadOptOutList` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List Survey Links](actions/list-survey-links.md) | `POST /publicapi/Survey/v3/ReadSurveyLinks` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List Surveys](actions/list-surveys.md) | `POST /publicapi/Survey/v3/ReadSurveyList` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List WebHooks](actions/list-web-hooks.md) | `POST /publicapi/WebHook/v3/ReadWebHookList` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List Workflow Transitions](actions/list-workflow-transitions.md) | `POST /publicapi/Workflow/v3/ReadWorkflowTransitions` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [List Workspaces](actions/list-workspaces.md) | `POST /publicapi/Survey/v3/ReadWorkspaceList` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Redeem Incentive Code](actions/redeem-incentive-code.md) | `POST /publicapi/Incentive/v3/RedeemIncentiveCode` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Remind Members](actions/remind-members.md) | `POST /publicapi/Distribute/v3/RemindMembers` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Update Members](actions/update-members.md) | `POST /publicapi/Panel/v3/UpdateMembers` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Update Opt-Outs](actions/update-opt-outs.md) | `POST /publicapi/Distribute/v3/WriteOptOutList` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Update Panel](actions/update-panel.md) | `POST /publicapi/Panel/v3/UpdatePanel` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Update Survey](actions/update-survey.md) | `POST /publicapi/Survey/v3/UpdateSurvey` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
| [Update WebHook](actions/update-web-hook.md) | `POST /publicapi/WebHook/v3/UpdateWebHook` | [docs](https://developer.survalyzer.com/knowledge-base/public-api-eu/) |
