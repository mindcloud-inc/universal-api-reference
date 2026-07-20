# Avionte: Native API Reference

A consolidated summary of Avionte's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://developer.avionte.com/reference
- **API base URL:** `https://api.avionte.com/`

## Authentication

### Partner OAuth 2.0

Use your Avionte tenant, API key, client ID, and client secret to obtain a partner access token.

### Credentials

- **Tenant ID:** `tenantId` · optional · Tenant code used in the Avionte Tenant header for Front Office and related API requests.
- **API Key:** `apiKey` · optional · Avionte partner API key used on token and resource requests.
- **Client ID:** `clientId` · optional · Partner OAuth client ID used when requesting an access token from Avionte.
- **Client Secret:** `clientSecret` · optional · Partner OAuth client secret used when requesting an access token from Avionte.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.avionte.com/authorize/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `avionte.aero.compasintegrationservice`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://developer.avionte.com/reference/avionteapikeyauth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Shared parameters:

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tenant` | query | `string` | no |

## Retry behavior

Wait 60000 ms before the first retry. Multiply the delay by 3 after each failed attempt.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Talent to Pipeline Stage](actions/add-talent-to-pipeline-stage.md) | `POST front-office/v1/pipeline/talent-stage/add` | [docs](https://developer.avionte.com/reference/addtalentpipelinestage) |
| [Create Talent Activity](actions/create-talent-activity.md) | `POST front-office/v1/talent/:talentId/activity` | [docs](https://developer.avionte.com/reference/createtalentactivity) |
| [Create Talent Tag](actions/create-talent-tag.md) | `POST front-office/v1/talent/:talentId/talenttag` | [docs](https://developer.avionte.com/reference/addtalenttag) |
| [Get a Company](actions/get-a-company.md) | `GET front-office/v1/company/:companyId` | [docs](https://developer.avionte.com/reference/getcompany) |
| [Get a Contact](actions/get-a-contact.md) | `GET front-office/v1/contact/:contactId` | [docs](https://developer.avionte.com/reference/getcontact) |
| [Get a Department](actions/get-a-department.md) | `GET front-office/v1/department/:departmentId` | [docs](https://developer.avionte.com/reference/getdepartment) |
| [Get a Job](actions/get-a-job.md) | `GET front-office/v1/job/:jobId` | [docs](https://developer.avionte.com/reference/getjob) |
| [Get a List of Talent Assessments](actions/get-a-list-of-talent-assessments.md) | `GET front-office/v1/talent/:talentId/assessments` | [docs](https://developer.avionte.com/reference/gettalentassessment) |
| [Get a Placement](actions/get-a-placement.md) | `GET front-office/v1/placement/:placementId` | [docs](https://developer.avionte.com/reference/gethire) |
| [Get a Talent Nomination Stage](actions/get-a-talent-nomination-stage.md) | `GET front-office/v1/talent/stage/:nominationId` | [docs](https://developer.avionte.com/reference/gettalentstage) |
| [Get Applicant Posted Jobs](actions/get-applicant-posted-jobs.md) | `GET front-office/v1/webapplicants/talent/:talentId/posted-jobs` | [docs](https://developer.avionte.com/reference/getapplicantpostedjobs) |
| [Get Available Talent Statuses](actions/get-available-talent-statuses.md) | `GET front-office/v1/talent-statuses` | [docs](https://developer.avionte.com/reference/getavailabletalentstatuses) |
| [Get Branches](actions/get-branches.md) | `GET front-office/v1/branch` | [docs](https://developer.avionte.com/reference/getbranches) |
| [Get Certificates](actions/get-certificates.md) | `GET front-office/v1/certificates` | [docs](https://developer.avionte.com/reference/certificates-1) |
| [Get Company IDs](actions/get-company-ids.md) | `GET front-office/v1/companies/ids/:page/:pageSize` | [docs](https://developer.avionte.com/reference/companyids) |
| [Get Contact IDs](actions/get-contact-ids.md) | `GET front-office/v1/contacts/ids/:page/:pageSize` | [docs](https://developer.avionte.com/reference/contactids) |
| [Get Department IDs](actions/get-department-ids.md) | `GET front-office/v1/departments/ids/:page/:pageSize` | [docs](https://developer.avionte.com/reference/get-department-ids) |
| [Get Job IDs](actions/get-job-ids.md) | `GET front-office/v1/jobs/ids/:page/:pageSize` | [docs](https://developer.avionte.com/reference/jobids) |
| [Get Placement IDs](actions/get-placement-ids.md) | `GET front-office/v1/placements/ids/:page/:pageSize` | [docs](https://developer.avionte.com/reference/placementids) |
| [Get Skill Positions](actions/get-skill-positions.md) | `GET front-office/v1/skill-positions` | [docs](https://developer.avionte.com/reference/getskillpositions) |
| [Get Talent Document Types](actions/get-talent-document-types.md) | `GET front-office/v1/talent-document-types` | [docs](https://developer.avionte.com/reference/gettalentdocumenttypes) |
| [Get Talent Documents](actions/get-talent-documents.md) | `GET /front-office/v1/talent/:talentId/document` | [docs](https://developer.avionte.com/reference/gettalentdocuments) |
| [Get Talent IDs](actions/get-talent-ids.md) | `GET front-office/v1/talents/ids/:page/:pageSize` | [docs](https://developer.avionte.com/reference/talentids) |
| [Get Talent Onboarding Tasks](actions/get-talent-onboarding-tasks.md) | `GET front-office/v1/talent/:talentId/talent-onboarding-tasks` | [docs](https://developer.avionte.com/reference/gettalentonbordingtasks) |
| [Get Talent Referrals](actions/get-talent-referrals.md) | `GET front-office/v1/talent/:talentId/talent-referrals` | [docs](https://developer.avionte.com/reference/gettalentreferrals) |
| [Get Talent Skills](actions/get-talent-skills.md) | `GET front-office/v1/talent/:talentId/skills` | [docs](https://developer.avionte.com/reference/gettalentskills) |
| [Get Talent Tags](actions/get-talent-tags.md) | `GET /front-office/v1/talent/:talentId/all-tags` | [docs](https://developer.avionte.com/reference/get-all-talent-tags) |
| [Get Web Applicants for a Job](actions/get-web-applicants-for-a-job.md) | `GET front-office/v1/webapplicants/job/:jobId` | [docs](https://developer.avionte.com/reference/get-web-applicants-for-job) |
| [Get Web Applications for a Talent](actions/get-web-applications-for-a-talent.md) | `GET front-office/v1/webapplicants/talent/:talentId` | [docs](https://developer.avionte.com/reference/get-web-applications-for-talent) |
| [Query Multiple Jobs](actions/query-multiple-jobs.md) | `POST front-office/v1/jobs/multi-query` | [docs](https://developer.avionte.com/reference/querymultiplejobs) |
| [Query Multiple Talents](actions/query-multiple-talents.md) | `POST front-office/v1/talents/multi-query` | [docs](https://developer.avionte.com/reference/querymultipletalents) |
| [Query Multiple Web Applicants](actions/query-multiple-web-applicants.md) | `POST https://api.avionte.com/front-office/v1/webapplicants/job/multi-query` | [docs](https://developer.avionte.com/reference/querymultiplewebapplicants) |
| [Update Talent](actions/update-talent.md) | `PUT front-office/v1/talent/:talentId` | [docs](https://developer.avionte.com/reference/updatetalent) |
