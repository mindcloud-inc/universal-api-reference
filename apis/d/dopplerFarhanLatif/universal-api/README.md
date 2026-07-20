# <img src="https://images.mindcloud.co/apps/icons/ca504eb965b366981679016924e0d709deb6768f-563x108_1777497589297.png" alt="Doppler Farhan Latif logo" width="28" height="28"> Doppler Farhan Latif: Universal API

Manage secrets and app configuration

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dopplerFarhanLatif/latest
- **Category:** IT Operations / DevOps
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.doppler.com
- **Vendor API docs:** https://docs.doppler.com/reference/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerFarhanLatif/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Config Log](actions/get-config-log.md) | GET | Retrieves a config log from Doppler. |
| [List Config Logs](actions/list-config-logs.md) | GET | Retrieves config logs from Doppler. |

### Config

| Action | Method | Description |
| --- | --- | --- |
| [Get Config](actions/get-config.md) | GET | Retrieves config details from Doppler. |
| [List Configs](actions/list-configs.md) | GET | Retrieves configs from a Doppler project. |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [List Environments](actions/list-environments.md) | GET | Retrieves environments from a Doppler project. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves project details from Doppler. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Doppler. |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Delete Secret](actions/delete-secret.md) | DELETE | Deletes an existing secret from a Doppler config. |
| [Get Secret](actions/get-secret.md) | GET | Retrieves a secret from a Doppler config. |
| [List Secret Names](actions/list-secret-names.md) | GET | Retrieves secret names from a Doppler config. |
| [List Secrets](actions/list-secrets.md) | GET | Retrieves secrets from a Doppler config. |
| [Update Secret Note](actions/update-secret-note.md) | PUT | Updates a secret note in Doppler. |
| [Update Secrets](actions/update-secrets.md) | PUT | Updates or creates secrets in a Doppler config. |

