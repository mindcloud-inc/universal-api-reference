# Testlify: Native API Reference

A consolidated summary of Testlify's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.testlify.com/reference
- **API base URL:** `https://api.testlify.com`

## Authentication

### API Key

Authenticate with a Testlify workspace access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.testlify.com/docs/how-to-generate-and-use-an-access-token-in-testlify)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 50; minimum 1). Use `skip` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `colName` in the query string. Set the direction separately with `inOrder`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Access Token](actions/create-access-token.md) | `POST /v1/workspace/accesstoken/generate` | [docs](https://docs.testlify.com/reference/generate_access_token) |
| [Create Assessment From Template](actions/create-assessment-from-template.md) | `POST /v1/reseller/assessment` | [docs](https://docs.testlify.com/reference/create_assessment_from_template) |
| [Create Compose Assessment](actions/create-compose-assessment.md) | `POST /v1/assessment/compose` | [docs](https://docs.testlify.com/reference/create_compose_assessment) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/webhook` | [docs](https://docs.testlify.com/reference/create_webhook) |
| [Get Assessment](actions/get-assessment.md) | `GET /v1/assessment/:assessmentId` | [docs](https://docs.testlify.com/reference/get_single_assessment) |
| [Get Candidate Result](actions/get-candidate-result.md) | `GET /v1/assessment/:assessmentId/candidate/:candidateId` | [docs](https://docs.testlify.com/reference/get_candidate_result) |
| [Get Question](actions/get-question.md) | `GET /v1/question/:questionId` | [docs](https://docs.testlify.com/reference/get_question_details) |
| [Invite Candidates](actions/invite-candidates.md) | `POST /v1/assessment/candidate/invites` | [docs](https://docs.testlify.com/reference/invite_candidates) |
| [Invite Workspace Users](actions/invite-workspace-users.md) | `POST /v1/workspace/invite/user` | [docs](https://docs.testlify.com/reference/invite_workspace_users) |
| [List Access Tokens](actions/list-access-tokens.md) | `GET /v1/workspace/accesstokens` | [docs](https://docs.testlify.com/reference/get_access_tokens) |
| [List Assessment Candidates](actions/list-assessment-candidates.md) | `GET /v1/assessment/:assessmentId/candidate` | [docs](https://docs.testlify.com/reference/get_all_candidates) |
| [List Assessments](actions/list-assessments.md) | `GET /v1/assessment` | [docs](https://docs.testlify.com/reference/get_all_assessments) |
| [List Candidate Assessments](actions/list-candidate-assessments.md) | `GET /v1/assessment/:candidateId/assessments` | [docs](https://docs.testlify.com/reference/get_candidate_assessments) |
| [List Candidates](actions/list-candidates.md) | `GET /v1/candidate` | [docs](https://docs.testlify.com/reference/get_candidate_list) |
| [List Coding Languages](actions/list-coding-languages.md) | `GET /v1/assessment/coding/language` | [docs](https://docs.testlify.com/reference/get_coding_languages) |
| [List Industry Types](actions/list-industry-types.md) | `GET /v1/static/testlibrary/industry/types` | [docs](https://docs.testlify.com/reference/get_industry_types) |
| [List Job Roles](actions/list-job-roles.md) | `GET /v1/workspace/jobrole` | [docs](https://docs.testlify.com/reference/get_job_roles) |
| [List Questions](actions/list-questions.md) | `GET /v1/question` | [docs](https://docs.testlify.com/reference/get_questions) |
| [List Test Libraries](actions/list-test-libraries.md) | `GET /v1/test/library/search` | [docs](https://docs.testlify.com/reference/get_test_libraries) |
| [List Test Library Types](actions/list-test-library-types.md) | `GET /v1/static/testlibrary/type` | [docs](https://docs.testlify.com/reference/get_test_library_types) |
| [List Workspace Users](actions/list-workspace-users.md) | `GET /v1/workspace/team` | [docs](https://docs.testlify.com/reference/get_workspace_users) |
