# <img src="https://images.mindcloud.co/apps/icons/murf-dub_1774361549035.png" alt="Murf Dub logo" width="28" height="28"> Murf Dub: Universal API

Create, track, and manage dubbed media jobs and projects

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/murfDub/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dub.murf.ai
- **Vendor API docs:** https://murf.ai/api/docs/capabilities/dubbing

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Destination Languages](actions/list-destination-languages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/list-destination-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Dub

| Action | Method | Description |
| --- | --- | --- |
| [Create Dubbing Job With Project ID](actions/create-dubbing-job-with-project-id.md) | POST | Creates a dubbing job in Murf Dub from a project. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Dubbing Job](actions/create-dubbing-job.md) | POST | Creates a dubbing job in Murf Dub. |

### Languages

| Action | Method | Description |
| --- | --- | --- |
| [List Destination Languages](actions/list-destination-languages.md) | GET | Retrieves destination languages from Murf Dub. |
| [List Source Languages](actions/list-source-languages.md) | GET | Retrieves source languages from Murf Dub. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Dubbing Project](actions/create-dubbing-project.md) | POST | Creates a dubbing project in Murf Dub. |
| [List Dubbing Projects](actions/list-dubbing-projects.md) | GET | Retrieves dubbing projects from Murf Dub. |
| [Update Dubbing Project](actions/update-dubbing-project.md) | PUT | Updates a dubbing project in Murf Dub. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Dubbing Job Status](actions/get-dubbing-job-status.md) | GET | Retrieves a Murf Dub job status. |

