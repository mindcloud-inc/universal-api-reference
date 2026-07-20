# <img src="https://images.mindcloud.co/apps/icons/crew-mem_1774960797563.png" alt="CrewMem logo" width="28" height="28"> CrewMem: Universal API

Manage teams, members, and AI team memories.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/crewMem/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://crewmem.com
- **Vendor API docs:** https://crewmem.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Memory Jobs](actions/list-memory-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/list-memory-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Member](actions/create-member.md) | POST |  |
| [Delete Member](actions/delete-member.md) | DELETE |  |

### Memory

| Action | Method | Description |
| --- | --- | --- |
| [Add Memory](actions/add-memory.md) | POST |  |
| [Create Memory](actions/create-memory.md) | POST |  |

### Memory Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Memory Job](actions/get-memory-job.md) | GET |  |
| [List Memory Jobs](actions/list-memory-jobs.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST |  |
| [Delete Team](actions/delete-team.md) | DELETE |  |

### Team Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Team Member](actions/create-team-member.md) | POST |  |
| [Delete Team Member](actions/delete-team-member.md) | DELETE |  |

