# <img src="https://images.mindcloud.co/apps/icons/hitl_1775852853556.png" alt="HITL Platform logo" width="28" height="28"> HITL Platform: Universal API

HITL.sh routes reviews and approvals to human reviewers through loops and requests, giving teams API access for loop management, request submission, and response handling.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hITLPlatform/latest
- **Category:** Productivity / Project Management
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hitl.sh/
- **Vendor API docs:** https://docs.hitl.sh/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test API Key](actions/test-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Request Feedback](actions/add-request-feedback.md) | POST |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Loop](actions/create-loop.md) | POST |  |
| [Delete Loop](actions/delete-loop.md) | DELETE |  |
| [Get Loop](actions/get-loop.md) | GET |  |
| [List Loops](actions/list-loops.md) | GET |  |
| [Update Loop](actions/update-loop.md) | PUT |  |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [List Loop Members](actions/list-loop-members.md) | GET |  |
| [Remove Loop Member](actions/remove-loop-member.md) | DELETE |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Request](actions/cancel-request.md) | DELETE |  |
| [Create Request](actions/create-request.md) | POST |  |
| [Get Request](actions/get-request.md) | GET |  |
| [List Loop Requests](actions/list-loop-requests.md) | GET |  |
| [List Requests](actions/list-requests.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Test API Key](actions/test-api-key.md) | GET |  |

