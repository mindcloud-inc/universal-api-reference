# <img src="https://images.mindcloud.co/apps/icons/test-dome_1774462027387.png" alt="TestDome logo" width="28" height="28"> TestDome: Universal API

Connect TestDome to manage screening tests, candidates, invitations, reports, and test settings from the TestDome API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/testDome/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.testdome.com
- **Vendor API docs:** https://api.testdome.com/openapi-ui/index/index.html?urls.primaryName=v3%20Docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Plan](actions/get-current-plan.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-current-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Plan](actions/get-current-plan.md) | GET | Retrieves the current plan from TestDome. |

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [Archive Candidates](actions/archive-candidates.md) | PUT | Archives candidates in TestDome. |
| [Create Candidate Sharing URL](actions/create-candidate-sharing-url.md) | POST | Creates a candidate sharing URL in TestDome. |
| [Create Test Candidates Share URL](actions/create-test-candidates-share-url.md) | POST | Creates a share URL for test candidates in TestDome. |
| [Extend Test Candidate Deadline](actions/extend-test-candidate-deadline.md) | PUT | Extends test candidate deadlines in TestDome. |
| [Get Candidate](actions/get-candidate.md) | GET | Retrieves a candidate from TestDome. |
| [List Candidates](actions/list-candidates.md) | GET | Retrieves candidates from TestDome. |
| [List Test Candidates](actions/list-test-candidates.md) | GET | Retrieves test candidates from TestDome. |
| [Notify Test Candidates](actions/notify-test-candidates.md) | PUT | Notifies test candidates in TestDome. |
| [Unarchive Candidates](actions/unarchive-candidates.md) | PUT | Unarchives candidates in TestDome. |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Candidate Invite](actions/cancel-candidate-invite.md) | PUT | Cancels a candidate invite in TestDome. |
| [Invite Candidates Via Email](actions/invite-candidates-via-email.md) | POST | Invites candidates via email in TestDome. |

### Test

| Action | Method | Description |
| --- | --- | --- |
| [Archive Test](actions/archive-test.md) | PUT | Archives a test in TestDome. |
| [Delete Test](actions/delete-test.md) | DELETE | Deletes an existing test from TestDome. |
| [Get Test](actions/get-test.md) | GET | Retrieves a test from TestDome. |
| [Get Test Settings](actions/get-test-settings.md) | GET | Retrieves test settings from TestDome. |
| [List Tests](actions/list-tests.md) | GET | Retrieves tests from TestDome. |
| [Provide Test Proctoring Consent](actions/provide-test-proctoring-consent.md) | PUT | Provides proctoring consent for test candidates in TestDome. |
| [Unarchive Test](actions/unarchive-test.md) | PUT | Unarchives a test in TestDome. |
| [Update Test Cutoff Score](actions/update-test-cutoff-score.md) | PUT | Updates a test cutoff score in TestDome. |
| [Update Test Settings](actions/update-test-settings.md) | PUT | Updates test settings in TestDome. |
| [Update Test URL Settings](actions/update-test-url-settings.md) | PUT | Updates test URL settings in TestDome. |

### Test Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Test URL](actions/create-test-url.md) | POST | Creates a new test URL in TestDome. |
| [Update Test URL](actions/update-test-url.md) | PUT | Updates an existing test URL in TestDome. |

