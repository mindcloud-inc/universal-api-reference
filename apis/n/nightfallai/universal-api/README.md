# <img src="https://images.mindcloud.co/apps/icons/favicon-help-nightfall-ai-48x48_1775763090190.png" alt="Nightfall.ai logo" width="28" height="28"> Nightfall.ai: Universal API

Scan content, manage violations, and review Nightfall security events

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nightfallai/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nightfall.ai
- **Vendor API docs:** https://help.nightfall.ai/developer-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Violations](actions/list-violations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-violations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Actor Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Exfiltration Actor Activity](actions/get-exfiltration-actor-activity.md) | GET | Retrieves activity for an exfiltration actor from Nightfall.ai. |
| [Get Posture Actor Activity](actions/get-posture-actor-activity.md) | GET | Retrieves activity for a posture actor from Nightfall.ai. |

### Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Annotate Finding](actions/annotate-finding.md) | PUT | Updates a finding annotation in Nightfall.ai. |
| [Get Annotation](actions/get-annotation.md) | GET | Retrieves an annotation from Nightfall.ai. |
| [Remove Finding Annotation](actions/remove-finding-annotation.md) | DELETE | Deletes a finding annotation from Nightfall.ai. |

### Asset Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Exfiltration Asset Activity](actions/get-exfiltration-asset-activity.md) | GET | Retrieves activity for an exfiltration asset from Nightfall.ai. |
| [Get Posture Asset Activity](actions/get-posture-asset-activity.md) | GET | Retrieves activity for a posture asset from Nightfall.ai. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Endpoint Devices](actions/list-endpoint-devices.md) | GET | Retrieves endpoint devices from Nightfall.ai. |

### Exfiltration Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Exfiltration Event Activity](actions/get-exfiltration-event-activity.md) | GET | Retrieves activity for an exfiltration event from Nightfall.ai. |

### Exfiltration Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Exfiltration Event](actions/get-exfiltration-event.md) | GET | Retrieves an exfiltration event from Nightfall.ai. |
| [List Exfiltration Events](actions/list-exfiltration-events.md) | GET | Retrieves exfiltration events from Nightfall.ai. |
| [Search Exfiltration Events](actions/search-exfiltration-events.md) | GET | Finds exfiltration events in Nightfall.ai by filters. |

### File Scan Job

| Action | Method | Description |
| --- | --- | --- |
| [Scan Uploaded File](actions/scan-uploaded-file.md) | POST | Scans an uploaded file with Nightfall.ai. |

### File Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create File Upload](actions/create-file-upload.md) | POST | Creates a file upload in Nightfall.ai. |
| [Finish File Upload](actions/finish-file-upload.md) | PUT | Finishes a file upload in Nightfall.ai. |
| [Upload File Chunk](actions/upload-file-chunk.md) | PUT | Uploads a file chunk to Nightfall.ai. |

### Finding

| Action | Method | Description |
| --- | --- | --- |
| [Get Violation Findings](actions/get-violation-findings.md) | GET | Retrieves findings for a violation from Nightfall.ai. |

### Policy Scope

| Action | Method | Description |
| --- | --- | --- |
| [Update Policy Domain Scope](actions/update-policy-domain-scope.md) | PUT | Updates a policy domain scope in Nightfall.ai. |
| [Update Policy User Scope](actions/update-policy-user-scope.md) | PUT | Updates a policy user scope in Nightfall.ai. |

### Posture Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Posture Event Activity](actions/get-posture-event-activity.md) | GET | Retrieves activity for a posture event from Nightfall.ai. |

### Posture Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Posture Event](actions/get-posture-event.md) | GET | Retrieves a posture event from Nightfall.ai. |
| [List Posture Events](actions/list-posture-events.md) | GET | Retrieves posture events from Nightfall.ai. |
| [Search Posture Events](actions/search-posture-events.md) | GET | Finds posture events in Nightfall.ai by filters. |

### Repository

| Action | Method | Description |
| --- | --- | --- |
| [List GitHub Repositories](actions/list-git-hub-repositories.md) | GET | Retrieves GitHub repositories from Nightfall.ai. |

### Scan Result

| Action | Method | Description |
| --- | --- | --- |
| [Scan Text](actions/scan-text.md) | POST | Scans text for sensitive data with Nightfall.ai. |

### Violation

| Action | Method | Description |
| --- | --- | --- |
| [Get Violation](actions/get-violation.md) | GET | Retrieves a violation from Nightfall.ai. |
| [List Violations](actions/list-violations.md) | GET | Retrieves violations from Nightfall.ai. |
| [Search Violations](actions/search-violations.md) | GET | Finds violations in Nightfall.ai by search filters. |
| [Take Action on Violations](actions/take-action-on-violations.md) | PUT | Updates violations by applying actions in Nightfall.ai. |

### Violation Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Violation Activity](actions/get-violation-activity.md) | GET | Retrieves activity for a violation from Nightfall.ai. |

