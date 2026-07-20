# <img src="https://images.mindcloud.co/apps/icons/tiledesk-icon-square-padded_1776187490165.png" alt="Tiledesk logo" width="28" height="28"> Tiledesk: Universal API

Tiledesk is a customer service platform for live chat, ticketing, chatbots, and support-team management. This app wraps Tiledesk REST APIs for requests, leads, messages, projects, teammates, tags, events, labels, files, segments, chatbots, departments, and groups.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tiledesk/latest
- **Category:** Support / Ticketing
- **Actions:** 66
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tiledesk.com
- **Vendor API docs:** https://developer.tiledesk.com/apis/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project Details](actions/get-project-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/get-project-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (66)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Lists activities in the current Tiledesk project. |

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot](actions/create-bot.md) | POST | Creates a bot in the current Tiledesk project. |
| [Delete Bot](actions/delete-bot.md) | DELETE | Deletes a bot from the current Tiledesk project. |
| [Get Bot](actions/get-bot.md) | GET | Retrieves a bot from the current Tiledesk project. |
| [List Bots](actions/list-bots.md) | GET | Lists bots in the current Tiledesk project. |
| [Update Bot](actions/update-bot.md) | PUT | Updates a bot in the current Tiledesk project. |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [Create Department](actions/create-department.md) | POST | Creates a department in the current Tiledesk project. |
| [Delete Department](actions/delete-department.md) | DELETE | Deletes a department from the current Tiledesk project. |
| [Get Department](actions/get-department.md) | GET | Retrieves a department from the current Tiledesk project. |
| [List All Departments](actions/list-all-departments.md) | GET | Lists all departments in the current Tiledesk project. |
| [List Departments](actions/list-departments.md) | GET | Lists active departments in the current Tiledesk project. |
| [Update Department](actions/update-department.md) | PUT | Updates a department in the current Tiledesk project. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates an event in the current Tiledesk project. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from the current Tiledesk project. |
| [List Events](actions/list-events.md) | GET | Lists events in the current Tiledesk project. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from the current Tiledesk project. |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot Intent](actions/create-bot-intent.md) | POST | Creates a bot intent in the current Tiledesk project. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Delete Labels By Language](actions/delete-labels-by-language.md) | DELETE | Deletes labels for a language from Tiledesk. |
| [Get Labels By Language](actions/get-labels-by-language.md) | GET | Retrieves labels for a language from Tiledesk. |
| [List Labels](actions/list-labels.md) | GET | Lists labels in the current Tiledesk project. |
| [Upsert Labels By Language](actions/upsert-labels-by-language.md) | PUT | Upserts labels for a language in Tiledesk. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from the current Tiledesk project. |
| [List Leads](actions/list-leads.md) | GET | Lists leads in the current Tiledesk project. |
| [Update Lead](actions/update-lead.md) | PUT | Updates a lead in the current Tiledesk project. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get Request History](actions/get-request-history.md) | GET | Retrieves message history for a request from Tiledesk. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Check Project Open Status](actions/check-project-open-status.md) | GET | Retrieves the current project's open status from Tiledesk. |
| [Get Project Details](actions/get-project-details.md) | GET | Retrieves details for the current project from Tiledesk. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Average Waiting Response Time](actions/get-average-waiting-response-time.md) | GET | Retrieves average waiting response times from Tiledesk. |
| [Get Conversation Count](actions/get-conversation-count.md) | GET | Retrieves the conversation count from Tiledesk. |
| [Get Conversation Count By Day](actions/get-conversation-count-by-day.md) | GET | Retrieves daily conversation counts from Tiledesk. |
| [Get Conversation Count By Hour](actions/get-conversation-count-by-hour.md) | GET | Retrieves hourly conversation counts from Tiledesk. |
| [Get Conversation Count By Month](actions/get-conversation-count-by-month.md) | GET | Retrieves monthly conversation counts from Tiledesk. |
| [Get Conversation Count By Status](actions/get-conversation-count-by-status.md) | GET | Retrieves conversation counts by status from Tiledesk. |
| [Get Conversation Count By Week](actions/get-conversation-count-by-week.md) | GET | Retrieves weekly conversation counts from Tiledesk. |
| [Get Conversation Duration](actions/get-conversation-duration.md) | GET | Retrieves conversation duration metrics from Tiledesk. |
| [Get Customer Satisfaction](actions/get-customer-satisfaction.md) | GET | Retrieves customer satisfaction metrics from Tiledesk. |
| [Get Daily Waiting Response Time](actions/get-daily-waiting-response-time.md) | GET | Retrieves daily waiting response times from Tiledesk. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST | Creates a segment in the current Tiledesk project. |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes a segment from the current Tiledesk project. |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from the current Tiledesk project. |
| [List Segments](actions/list-segments.md) | GET | Lists segments in the current Tiledesk project. |
| [Update Segment](actions/update-segment.md) | PUT | Updates a segment in the current Tiledesk project. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a tag in the current Tiledesk project. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes a tag from the current Tiledesk project. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from the current Tiledesk project. |
| [List Tags](actions/list-tags.md) | GET | Lists tags in the current Tiledesk project. |
| [Update Tag](actions/update-tag.md) | PUT | Updates a tag in the current Tiledesk project. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Canned Response](actions/create-canned-response.md) | POST | Creates a canned response in the current Tiledesk project. |
| [Delete Canned Response](actions/delete-canned-response.md) | DELETE | Deletes a canned response from the current Tiledesk project. |
| [Get Canned Response](actions/get-canned-response.md) | GET | Retrieves a canned response from the current Tiledesk project. |
| [List Canned Responses](actions/list-canned-responses.md) | GET | Lists canned responses in the current Tiledesk project. |
| [Update Canned Response](actions/update-canned-response.md) | PUT | Updates a canned response in the current Tiledesk project. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Close Request](actions/close-request.md) | PUT | Closes a request in the current Tiledesk project. |
| [Create Request](actions/create-request.md) | POST | Creates a request in the current Tiledesk project. |
| [Get Request](actions/get-request.md) | GET | Retrieves a request from the current Tiledesk project. |
| [List Requests](actions/list-requests.md) | GET | Lists requests in the current Tiledesk project. |
| [Move Request To Agent](actions/move-request-to-agent.md) | PUT | Assigns a request to an agent in Tiledesk. |
| [Route Request To Department](actions/route-request-to-department.md) | PUT | Routes a request to a department in Tiledesk. |
| [Update Request Attributes](actions/update-request-attributes.md) | PUT | Updates a request's attributes in Tiledesk. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Tiledesk. |
| [Get Team Member](actions/get-team-member.md) | GET | Retrieves a team member from the current Tiledesk project. |
| [List Available Agents](actions/list-available-agents.md) | GET | Lists available agents in the current Tiledesk project. |
| [List Team Members](actions/list-team-members.md) | GET | Lists team members in the current Tiledesk project. |
| [Update Current Teammate](actions/update-current-teammate.md) | PUT | Updates the current teammate in the Tiledesk project. |
| [Update Current User](actions/update-current-user.md) | PUT | Updates the current user in Tiledesk. |
| [Update Team Member](actions/update-team-member.md) | PUT | Updates a team member in the current Tiledesk project. |

