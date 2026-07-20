# <img src="https://images.mindcloud.co/apps/icons/survalyzer_1775145589249.png" alt="Survalyzer logo" width="28" height="28"> Survalyzer: Universal API

Survalyzer provides survey, panel, interview, distribution, artifact, and webhook operations for the EU data center public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/survalyzer/latest
- **Actions:** 43
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://survalyzer.com
- **Vendor API docs:** https://developer.survalyzer.com/knowledge-base/public-api-eu/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (43)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create And Invite Members](actions/create-and-invite-members.md) | POST |  |
| [Create Artifact](actions/create-artifact.md) | POST |  |
| [Create Members](actions/create-members.md) | POST |  |
| [Create Panel](actions/create-panel.md) | POST |  |
| [Create Survey](actions/create-survey.md) | POST |  |
| [Create WebHook](actions/create-web-hook.md) | POST |  |
| [Delete Artifact](actions/delete-artifact.md) | DELETE |  |
| [Delete Distributor](actions/delete-distributor.md) | DELETE |  |
| [Delete Interview](actions/delete-interview.md) | DELETE |  |
| [Delete Members](actions/delete-members.md) | DELETE |  |
| [Delete Panel](actions/delete-panel.md) | DELETE |  |
| [Delete Sampling Project](actions/delete-sampling-project.md) | DELETE |  |
| [Delete Survey](actions/delete-survey.md) | DELETE |  |
| [Delete WebHook](actions/delete-web-hook.md) | DELETE |  |
| [Execute Workflow Transition](actions/execute-workflow-transition.md) | PUT |  |
| [Get Credit Balance](actions/get-credit-balance.md) | GET |  |
| [Get Interview](actions/get-interview.md) | GET |  |
| [Get Panel](actions/get-panel.md) | GET |  |
| [Get Sampling Project](actions/get-sampling-project.md) | GET |  |
| [Get Survey](actions/get-survey.md) | GET |  |
| [Invite Members](actions/invite-members.md) | POST |  |
| [List Artifacts](actions/list-artifacts.md) | GET |  |
| [List Bounces](actions/list-bounces.md) | GET |  |
| [List Distributors](actions/list-distributors.md) | GET |  |
| [List Incentive Transactions](actions/list-incentive-transactions.md) | GET |  |
| [List Incentives](actions/list-incentives.md) | GET |  |
| [List Interviews](actions/list-interviews.md) | GET |  |
| [List Interviews Compact](actions/list-interviews-compact.md) | GET |  |
| [List Members](actions/list-members.md) | GET |  |
| [List Message Templates](actions/list-message-templates.md) | GET |  |
| [List Opt-Outs](actions/list-opt-outs.md) | GET |  |
| [List Survey Links](actions/list-survey-links.md) | GET |  |
| [List Surveys](actions/list-surveys.md) | GET |  |
| [List WebHooks](actions/list-web-hooks.md) | GET |  |
| [List Workflow Transitions](actions/list-workflow-transitions.md) | GET |  |
| [Redeem Incentive Code](actions/redeem-incentive-code.md) | POST |  |
| [Remind Members](actions/remind-members.md) | POST |  |
| [Update Members](actions/update-members.md) | PUT |  |
| [Update Opt-Outs](actions/update-opt-outs.md) | PUT |  |
| [Update Panel](actions/update-panel.md) | PUT |  |
| [Update Survey](actions/update-survey.md) | PUT |  |
| [Update WebHook](actions/update-web-hook.md) | PUT |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET |  |

