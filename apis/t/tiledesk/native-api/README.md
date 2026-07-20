# Tiledesk: Native API Reference

A consolidated summary of Tiledesk's API configuration and 66 documented operations, with links to official documentation.

- **Official docs:** https://developer.tiledesk.com/apis/rest-api
- **API base URL:** `https://api.tiledesk.com/v3`

## Authentication

### JWT Token

Authenticate to Tiledesk REST APIs with a full JWT token returned by the Tiledesk sign-in endpoints.

### Credentials

- **JWT Token:** `token` · required · Full Tiledesk authorization token including the `JWT ` prefix.
- **Project ID:** `projectId` · required · The Tiledesk project ID used in project-scoped REST routes.
- **User ID:** `userId` · optional · Optional Tiledesk user ID for user-scoped endpoints and saved defaults.
- **Workspace ID:** `workspaceId` · optional · Optional Tiledesk workspace ID when an endpoint or workflow needs the workspace identifier explicitly.

Send these headers with each API request:

```http
Authorization: <token>
```

[Official authentication documentation](https://developer.tiledesk.com/apis/rest-api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (66 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Project Open Status](actions/check-project-open-status.md) | `GET /projects/{{credentials.projectId}}/isopen` | [docs](https://developer.tiledesk.com/apis/rest-api/projects#return-if-the-project-is-open-regarding-operating-hours) |
| [Close Request](actions/close-request.md) | `PUT /{{credentials.projectId}}/requests/:requestId/close` | [docs](https://developer.tiledesk.com/apis/rest-api/requests) |
| [Create Bot](actions/create-bot.md) | `POST /{{credentials.projectId}}/faq_kb` | [docs](https://developer.tiledesk.com/apis/rest-api/bots) |
| [Create Bot Intent](actions/create-bot-intent.md) | `POST /{{credentials.projectId}}/faq` | [docs](https://developer.tiledesk.com/apis/rest-api/faq) |
| [Create Canned Response](actions/create-canned-response.md) | `POST /{{credentials.projectId}}/canned` | [docs](https://developer.tiledesk.com/apis/rest-api/canned-response) |
| [Create Department](actions/create-department.md) | `POST /{{credentials.projectId}}/departments` | [docs](https://developer.tiledesk.com/apis/rest-api/management-api/departments) |
| [Create Event](actions/create-event.md) | `POST /{{credentials.projectId}}/events` | [docs](https://developer.tiledesk.com/apis/rest-api/events) |
| [Create Request](actions/create-request.md) | `POST /{{credentials.projectId}}/requests` | [docs](https://developer.tiledesk.com/apis/rest-api/requests) |
| [Create Segment](actions/create-segment.md) | `POST /{{credentials.projectId}}/segments` | [docs](https://developer.tiledesk.com/apis/rest-api/segments) |
| [Create Tag](actions/create-tag.md) | `POST /{{credentials.projectId}}/tags` | [docs](https://developer.tiledesk.com/apis/rest-api/tags) |
| [Delete Bot](actions/delete-bot.md) | `DELETE /{{credentials.projectId}}/faq_kb/:botId` | [docs](https://developer.tiledesk.com/apis/rest-api/bots) |
| [Delete Canned Response](actions/delete-canned-response.md) | `DELETE /{{credentials.projectId}}/canned/:id` | [docs](https://developer.tiledesk.com/apis/rest-api/canned-response) |
| [Delete Department](actions/delete-department.md) | `DELETE /{{credentials.projectId}}/departments/:depId` | [docs](https://developer.tiledesk.com/apis/rest-api/management-api/departments) |
| [Delete Labels By Language](actions/delete-labels-by-language.md) | `DELETE /{{credentials.projectId}}/labels/:lang` | [docs](https://developer.tiledesk.com/apis/rest-api/labels) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /{{credentials.projectId}}/segments/:segmentId` | [docs](https://developer.tiledesk.com/apis/rest-api/segments) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /{{credentials.projectId}}/tags/:id` | [docs](https://developer.tiledesk.com/apis/rest-api/tags) |
| [Get Average Waiting Response Time](actions/get-average-waiting-response-time.md) | `GET /{{credentials.projectId}}/analytics/waiting_time/agents` | [docs](https://developer.tiledesk.com/apis/rest-api/analytics) |
| [Get Bot](actions/get-bot.md) | `GET /{{credentials.projectId}}/faq_kb/:botId` | [docs](https://developer.tiledesk.com/apis/rest-api/bots) |
| [Get Canned Response](actions/get-canned-response.md) | `GET /{{credentials.projectId}}/canned/:id` | [docs](https://developer.tiledesk.com/apis/rest-api/canned-response) |
| [Get Conversation Count](actions/get-conversation-count.md) | `GET /{{credentials.projectId}}/analytics/requests/count` | [docs](https://developer.tiledesk.com/apis/rest-api/analytics) |
| [Get Conversation Count By Day](actions/get-conversation-count-by-day.md) | `GET /{{credentials.projectId}}/analytics/requests/aggregate/day` | [docs](https://developer.tiledesk.com/apis/rest-api/analytics) |
| [Get Conversation Count By Hour](actions/get-conversation-count-by-hour.md) | `GET /{{credentials.projectId}}/analytics/requests/aggregate/hours` | [docs](https://developer.tiledesk.com/apis/rest-api/analytics) |
| [Get Conversation Count By Month](actions/get-conversation-count-by-month.md) | `GET /{{credentials.projectId}}/analytics/requests/aggregate/month` | [docs](https://developer.tiledesk.com/apis/rest-api/analytics) |
| [Get Conversation Count By Status](actions/get-conversation-count-by-status.md) | `GET /{{credentials.projectId}}/analytics/requests/aggregate/status` | [docs](https://developer.tiledesk.com/apis/rest-api/analytics) |
| [Get Conversation Count By Week](actions/get-conversation-count-by-week.md) | `GET /{{credentials.projectId}}/analytics/requests/aggregate/week` | [docs](https://developer.tiledesk.com/apis/rest-api/analytics) |
| [Get Conversation Duration](actions/get-conversation-duration.md) | `GET /{{credentials.projectId}}/analytics/requests/duration` | [docs](https://developer.tiledesk.com/apis/rest-api/analytics) |
| [Get Current User](actions/get-current-user.md) | `GET /users` | [docs](https://developer.tiledesk.com/apis/rest-api/user) |
| [Get Customer Satisfaction](actions/get-customer-satisfaction.md) | `GET /{{credentials.projectId}}/analytics/requests/satisfaction` | [docs](https://developer.tiledesk.com/apis/rest-api/analytics) |
| [Get Daily Waiting Response Time](actions/get-daily-waiting-response-time.md) | `GET /{{credentials.projectId}}/analytics/waiting_time/agents/day` | [docs](https://developer.tiledesk.com/apis/rest-api/analytics) |
| [Get Department](actions/get-department.md) | `GET /{{credentials.projectId}}/departments/:depId` | [docs](https://developer.tiledesk.com/apis/rest-api/management-api/departments#get-a-department-by-id) |
| [Get Event](actions/get-event.md) | `GET /{{credentials.projectId}}/events/:id` | [docs](https://developer.tiledesk.com/apis/rest-api/events) |
| [Get Group](actions/get-group.md) | `GET /{{credentials.projectId}}/groups/:groupId` | [docs](https://developer.tiledesk.com/apis/rest-api/management-api/groups#get-the-group-by-id) |
| [Get Labels By Language](actions/get-labels-by-language.md) | `GET /{{credentials.projectId}}/labels/:lang` | [docs](https://developer.tiledesk.com/apis/rest-api/labels) |
| [Get Lead](actions/get-lead.md) | `GET /{{credentials.projectId}}/leads/:leadId` | [docs](https://developer.tiledesk.com/apis/rest-api/leads#get-a-lead-by-id) |
| [Get Project Details](actions/get-project-details.md) | `GET /projects/{{credentials.projectId}}` | [docs](https://developer.tiledesk.com/apis/rest-api/projects) |
| [Get Request](actions/get-request.md) | `GET /{{credentials.projectId}}/requests/:requestId` | [docs](https://developer.tiledesk.com/apis/rest-api/requests) |
| [Get Request History](actions/get-request-history.md) | `GET /{{credentials.projectId}}/requests/:requestId/history` | [docs](https://developer.tiledesk.com/apis/rest-api/requests) |
| [Get Segment](actions/get-segment.md) | `GET /{{credentials.projectId}}/segments/:segmentId` | [docs](https://developer.tiledesk.com/apis/rest-api/segments) |
| [Get Tag](actions/get-tag.md) | `GET /{{credentials.projectId}}/tags/:id` | [docs](https://developer.tiledesk.com/apis/rest-api/tags) |
| [Get Team Member](actions/get-team-member.md) | `GET /{{credentials.projectId}}/project_users/users/:userId` | [docs](https://developer.tiledesk.com/apis/rest-api/team#get-the-team) |
| [List Activities](actions/list-activities.md) | `GET /{{credentials.projectId}}/activities` | [docs](https://developer.tiledesk.com/apis/rest-api/activities) |
| [List All Departments](actions/list-all-departments.md) | `GET /{{credentials.projectId}}/departments/allstatus` | [docs](https://developer.tiledesk.com/apis/rest-api/management-api/departments#get-all-departments-active-or-hidden) |
| [List Available Agents](actions/list-available-agents.md) | `GET /projects/{{credentials.projectId}}/users/availables` | [docs](https://developer.tiledesk.com/apis/rest-api/projects#return-the-available-agents) |
| [List Bots](actions/list-bots.md) | `GET /{{credentials.projectId}}/faq_kb` | [docs](https://developer.tiledesk.com/apis/rest-api/bots) |
| [List Canned Responses](actions/list-canned-responses.md) | `GET /{{credentials.projectId}}/canned` | [docs](https://developer.tiledesk.com/apis/rest-api/canned-response) |
| [List Departments](actions/list-departments.md) | `GET /{{credentials.projectId}}/departments` | [docs](https://developer.tiledesk.com/apis/rest-api/management-api/departments#get-all-active-departments) |
| [List Events](actions/list-events.md) | `GET /{{credentials.projectId}}/events` | [docs](https://developer.tiledesk.com/apis/rest-api/events) |
| [List Labels](actions/list-labels.md) | `GET /{{credentials.projectId}}/labels` | [docs](https://developer.tiledesk.com/apis/rest-api/labels) |
| [List Leads](actions/list-leads.md) | `GET /{{credentials.projectId}}/leads` | [docs](https://developer.tiledesk.com/apis/rest-api/leads) |
| [List Requests](actions/list-requests.md) | `GET /{{credentials.projectId}}/requests` | [docs](https://developer.tiledesk.com/apis/rest-api/requests) |
| [List Segments](actions/list-segments.md) | `GET /{{credentials.projectId}}/segments` | [docs](https://developer.tiledesk.com/apis/rest-api/segments) |
| [List Tags](actions/list-tags.md) | `GET /{{credentials.projectId}}/tags` | [docs](https://developer.tiledesk.com/apis/rest-api/tags) |
| [List Team Members](actions/list-team-members.md) | `GET /{{credentials.projectId}}/project_users` | [docs](https://developer.tiledesk.com/apis/rest-api/team#get-the-team) |
| [Move Request To Agent](actions/move-request-to-agent.md) | `PUT /{{credentials.projectId}}/requests/:requestId/agent` | [docs](https://developer.tiledesk.com/apis/rest-api/requests) |
| [Route Request To Department](actions/route-request-to-department.md) | `PUT /{{credentials.projectId}}/requests/:requestId/departments` | [docs](https://developer.tiledesk.com/apis/rest-api/requests) |
| [Update Bot](actions/update-bot.md) | `PUT /{{credentials.projectId}}/faq_kb/:botId` | [docs](https://developer.tiledesk.com/apis/rest-api/bots) |
| [Update Canned Response](actions/update-canned-response.md) | `PUT /{{credentials.projectId}}/canned/:id` | [docs](https://developer.tiledesk.com/apis/rest-api/canned-response) |
| [Update Current Teammate](actions/update-current-teammate.md) | `PUT /{{credentials.projectId}}/project_users/` | [docs](https://developer.tiledesk.com/apis/rest-api/team) |
| [Update Current User](actions/update-current-user.md) | `PUT /users/` | [docs](https://developer.tiledesk.com/apis/rest-api/user) |
| [Update Department](actions/update-department.md) | `PUT /{{credentials.projectId}}/departments/:depId` | [docs](https://developer.tiledesk.com/apis/rest-api/management-api/departments) |
| [Update Lead](actions/update-lead.md) | `PUT /{{credentials.projectId}}/leads/:leadId` | [docs](https://developer.tiledesk.com/apis/rest-api/leads) |
| [Update Request Attributes](actions/update-request-attributes.md) | `PUT /{{credentials.projectId}}/requests/:requestId/attributes` | [docs](https://developer.tiledesk.com/apis/rest-api/requests) |
| [Update Segment](actions/update-segment.md) | `PUT /{{credentials.projectId}}/segments/:segmentId` | [docs](https://developer.tiledesk.com/apis/rest-api/segments) |
| [Update Tag](actions/update-tag.md) | `PUT /{{credentials.projectId}}/tags/:id` | [docs](https://developer.tiledesk.com/apis/rest-api/tags) |
| [Update Team Member](actions/update-team-member.md) | `PUT /{{credentials.projectId}}/project_users/:projectUserId` | [docs](https://developer.tiledesk.com/apis/rest-api/team) |
| [Upsert Labels By Language](actions/upsert-labels-by-language.md) | `PUT /{{credentials.projectId}}/labels/:lang` | [docs](https://developer.tiledesk.com/apis/rest-api/labels) |
