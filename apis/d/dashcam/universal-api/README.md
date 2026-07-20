# <img src="https://images.mindcloud.co/apps/icons/dashcam_1775240023112.png" alt="Dashcam logo" width="28" height="28"> Dashcam: Universal API

Dashcam helps teams manage TestDriver replays, projects, test runs, usage, and supporting team settings from TestDriver's Dashcam console.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dashcam/latest
- **Category:** IT Operations / DevOps
- **Actions:** 47
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://testdriver.ai
- **Vendor API docs:** https://docs.testdriver.ai

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Billing Usage](actions/get-billing-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-billing-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (47)

### Build

| Action | Method | Description |
| --- | --- | --- |
| [Download Build](actions/download-build.md) | GET | Downloads a build from Dashcam. |

### Cache

| Action | Method | Description |
| --- | --- | --- |
| [Clear Cache](actions/clear-cache.md) | DELETE | Clears cache entries in Dashcam. |

### Cache Entry

| Action | Method | Description |
| --- | --- | --- |
| [Delete Cache By Prompt](actions/delete-cache-by-prompt.md) | DELETE | Deletes cache entries by prompt in Dashcam. |
| [Delete Cache Entry](actions/delete-cache-entry.md) | DELETE | Deletes a cache entry from Dashcam. |
| [List Cache Entries](actions/list-cache-entries.md) | GET | Retrieves cache entries from Dashcam. |

### Checkout Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Checkout Session](actions/create-checkout-session.md) | POST | Creates a checkout session in Dashcam. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a comment in Dashcam. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes a comment from Dashcam. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from Dashcam. |

### Coverage Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Coverage Report](actions/get-coverage-report.md) | GET | Retrieves a coverage report from Dashcam. |

### Interaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Cache Entry Interactions](actions/get-cache-entry-interactions.md) | GET | Retrieves interactions for a cache entry from Dashcam. |
| [Get Replay Interactions](actions/get-replay-interactions.md) | GET | Retrieves replay interactions from Dashcam. |
| [Get Test Case Interactions](actions/get-test-case-interactions.md) | GET | Retrieves interactions for a test case from Dashcam. |

### Log File

| Action | Method | Description |
| --- | --- | --- |
| [Download Log](actions/download-log.md) | GET | Downloads a log file from Dashcam. |

### Pending Invite

| Action | Method | Description |
| --- | --- | --- |
| [Remove Pending Invite](actions/remove-pending-invite.md) | DELETE | Removes a pending invite from Dashcam. |

### Performance Report

| Action | Method | Description |
| --- | --- | --- |
| [Download Replay Performance](actions/download-replay-performance.md) | GET | Downloads a replay performance report from Dashcam. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a project in Dashcam. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes a project from Dashcam. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Dashcam. |
| [Update Project](actions/update-project.md) | PUT | Updates a project in Dashcam. |

### Replay

| Action | Method | Description |
| --- | --- | --- |
| [Clone Replay](actions/clone-replay.md) | PUT | Clones a replay in Dashcam. |
| [Delete Replay](actions/delete-replay.md) | DELETE | Deletes a replay from Dashcam. |
| [Get Replay](actions/get-replay.md) | GET | Retrieves a replay from Dashcam. |
| [List Replays](actions/list-replays.md) | GET | Retrieves replays from Dashcam. |
| [Mark Replay Viewed](actions/mark-replay-viewed.md) | PUT | Marks a replay as viewed in Dashcam. |
| [Move Replay](actions/move-replay.md) | PUT | Moves a replay in Dashcam. |
| [Publish Replay](actions/publish-replay.md) | PUT | Publishes a replay in Dashcam. |
| [Save Replay Draft](actions/save-replay-draft.md) | PUT | Saves a replay draft in Dashcam. |

### Replay Access

| Action | Method | Description |
| --- | --- | --- |
| [Delete Replay Access](actions/delete-replay-access.md) | DELETE | Deletes replay access from Dashcam. |
| [Invite Replay Access](actions/invite-replay-access.md) | PUT | Invites a user to access a replay in Dashcam. |
| [Update Replay Access](actions/update-replay-access.md) | PUT | Updates replay access in Dashcam. |

### Replay Access Request

| Action | Method | Description |
| --- | --- | --- |
| [Request Replay Access](actions/request-replay-access.md) | POST | Requests access to a replay in Dashcam. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Usage](actions/get-billing-usage.md) | GET | Retrieves billing usage from Dashcam. |
| [Get Parallel Slots](actions/get-parallel-slots.md) | GET | Retrieves parallel slot details from Dashcam. |
| [Get Public Stats](actions/get-public-stats.md) | GET | Retrieves public stats from Dashcam. |
| [Get Testdriver Stats](actions/get-testdriver-stats.md) | GET | Retrieves TestDriver stats from Dashcam. |
| [List Usage Records](actions/list-usage-records.md) | GET | Retrieves usage records from Dashcam. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Portal Session](actions/get-portal-session.md) | GET | Retrieves a billing portal session from Dashcam. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves team details from Dashcam. |
| [Update Team Auto Join](actions/update-team-auto-join.md) | PUT | Updates team auto-join in Dashcam. |
| [Update Team Name](actions/update-team-name.md) | PUT | Updates a team name in Dashcam. |

### Team Invite

| Action | Method | Description |
| --- | --- | --- |
| [Invite Team Member](actions/invite-team-member.md) | POST | Invites a team member in Dashcam. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [Remove Team Member](actions/remove-team-member.md) | DELETE | Removes a team member from Dashcam. |

### Test Case

| Action | Method | Description |
| --- | --- | --- |
| [Get Replay Test Cases](actions/get-replay-test-cases.md) | GET | Retrieves test cases for a replay from Dashcam. |

### Test Result

| Action | Method | Description |
| --- | --- | --- |
| [List Testdriver Results](actions/list-testdriver-results.md) | GET | Retrieves TestDriver test results from Dashcam. |

### Test Suite

| Action | Method | Description |
| --- | --- | --- |
| [List Testdriver Suites](actions/list-testdriver-suites.md) | GET | Retrieves TestDriver suites from Dashcam. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Dashcam. |

