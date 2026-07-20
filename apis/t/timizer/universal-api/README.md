# <img src="https://images.mindcloud.co/apps/icons/timizer_1775769703985.png" alt="Timizer logo" width="28" height="28"> Timizer: Universal API

Manage timesheets, clients, missions, and activity reports in Timizer

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timizer/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://timizer.io
- **Vendor API docs:** https://api-doc.timizer.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Clients](actions/list-clients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activity Report

| Action | Method | Description |
| --- | --- | --- |
| [Create Team Activity Report](actions/create-team-activity-report.md) | POST | Creates a team activity report in Timizer. |
| [Get Team Activity Report](actions/get-team-activity-report.md) | GET | Retrieves a team activity report from Timizer. |
| [List Team Activity Reports](actions/list-team-activity-reports.md) | GET | Retrieves team activity reports from Timizer. |
| [Share Team Activity Report](actions/share-team-activity-report.md) | POST | Creates a share link for a team activity report in Timizer. |
| [Share Team Activity Report by Email](actions/share-team-activity-report-by-email.md) | POST | Shares a team activity report by email in Timizer. |
| [Update Team Activity Report](actions/update-team-activity-report.md) | PUT | Updates an existing team activity report in Timizer. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a client in Timizer. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Timizer. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Timizer. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Timizer. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Timizer. |

### Client Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Client Contact](actions/create-client-contact.md) | POST | Creates a client contact in Timizer. |
| [Delete Client Contact](actions/delete-client-contact.md) | DELETE | Deletes an existing client contact from Timizer. |
| [List Client Contacts](actions/list-client-contacts.md) | GET | Retrieves contacts for a client from Timizer. |

### Contracted Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Contracted Company](actions/create-contracted-company.md) | POST | Creates a contracted company in Timizer. |
| [Delete Contracted Company](actions/delete-contracted-company.md) | DELETE | Deletes an existing contracted company from Timizer. |
| [Get Contracted Company](actions/get-contracted-company.md) | GET | Retrieves a contracted company from Timizer. |
| [List Contracted Companies](actions/list-contracted-companies.md) | GET | Retrieves contracted companies from Timizer. |
| [Update Contracted Company](actions/update-contracted-company.md) | PUT | Updates an existing contracted company in Timizer. |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Create Team Invitations](actions/create-team-invitations.md) | POST | Creates team invitations and users if needed in Timizer. |

### Mission

| Action | Method | Description |
| --- | --- | --- |
| [Create Team Mission](actions/create-team-mission.md) | POST | Creates a team mission in Timizer. |
| [List Team Missions](actions/list-team-missions.md) | GET | Retrieves team missions from Timizer. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Timizer. |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team members from Timizer. |

