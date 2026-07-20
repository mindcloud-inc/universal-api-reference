# <img src="https://images.mindcloud.co/apps/icons/beatoven-icon-square_1775840335242.png" alt="Beatoven AI logo" width="28" height="28"> Beatoven AI: Universal API

Beatoven AI lets you generate AI music tracks from text prompts and check composition task status through Beatoven's public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/beatovenAI/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://beatoven.ai
- **Vendor API docs:** https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Task Status](actions/get-task-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/get-task-status?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Status](actions/get-task-status.md) | GET | Retrieves composition task status from Beatoven AI. |

### Track

| Action | Method | Description |
| --- | --- | --- |
| [Create Track](actions/create-track.md) | POST | Creates a new track in Beatoven AI from a text prompt. |

### Track Composition

| Action | Method | Description |
| --- | --- | --- |
| [Compose Track](actions/compose-track.md) | POST | Starts track composition in Beatoven AI from a text prompt. |

