# <img src="https://images.mindcloud.co/apps/icons/paradym_1775146536880.png" alt="Paradym logo" width="28" height="28"> Paradym: Universal API

Issue, verify, and manage digital credentials with Paradym

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/paradym/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://paradym.id
- **Vendor API docs:** https://paradym.id/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Archive Mdoc Credential Template](actions/archive-mdoc-credential-template.md) | DELETE | Archives an mdoc credential template in Paradym. |
| [Archive Presentation Template](actions/archive-presentation-template.md) | DELETE | Archives a presentation template in Paradym. |
| [Archive Sd-Jwt Vc Credential Template](actions/archive-sd-jwt-vc-credential-template.md) | DELETE | Archives an SD-JWT VC credential template in Paradym. |
| [Batch Revoke Credentials](actions/batch-revoke-credentials.md) | PUT | Revokes issued credentials in bulk in Paradym. |
| [Create Certificate](actions/create-certificate.md) | POST | Creates a certificate in Paradym. |
| [Create Mdoc Credential Template](actions/create-mdoc-credential-template.md) | POST | Creates an mdoc credential template in Paradym. |
| [List Certificates](actions/list-certificates.md) | GET | Retrieves a list of certificates from Paradym. |
| [List DIDs](actions/list-dids.md) | GET | Retrieves a list of DIDs from Paradym. |
| [List Issued Credentials](actions/list-issued-credentials.md) | GET | Retrieves issued credentials from Paradym. |
| [List Mdoc Credential Templates](actions/list-mdoc-credential-templates.md) | GET | Retrieves mdoc credential templates from Paradym. |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves project members from Paradym. |
| [List Trusted Entities](actions/list-trusted-entities.md) | GET | Retrieves a list of trusted entities from Paradym. |
| [Retrieve Default Profile](actions/retrieve-default-profile.md) | GET | Retrieves the default project profile from Paradym. |
| [Retrieve Mdoc Credential Template](actions/retrieve-mdoc-credential-template.md) | GET | Retrieves an mdoc credential template from Paradym. |
| [Retrieve Mdoc Credential Template JSON Schema](actions/retrieve-mdoc-credential-template-json-schema.md) | GET | Retrieves an mdoc credential template JSON schema from Paradym. |
| [Update Default Profile](actions/update-default-profile.md) | PUT | Updates the default project profile in Paradym. |
| [Update Mdoc Credential Template](actions/update-mdoc-credential-template.md) | PUT | Updates an mdoc credential template in Paradym. |

### Presentation Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Presentation Template](actions/create-presentation-template.md) | POST | Creates a presentation template in Paradym. |
| [List Presentation Templates](actions/list-presentation-templates.md) | GET | Retrieves presentation templates from Paradym. |
| [Retrieve Presentation Template](actions/retrieve-presentation-template.md) | GET | Retrieves a presentation template from Paradym. |
| [Update Presentation Template](actions/update-presentation-template.md) | PUT | Updates a presentation template in Paradym. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Paradym. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Paradym. |

### Sd-jwt Vc Credential Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Sd-Jwt Vc Credential Template](actions/create-sd-jwt-vc-credential-template.md) | POST | Creates an SD-JWT VC credential template in Paradym. |
| [List Sd-Jwt Vc Credential Templates](actions/list-sd-jwt-vc-credential-templates.md) | GET | Retrieves SD-JWT VC credential templates from Paradym. |
| [Retrieve Sd-Jwt Vc Credential Template](actions/retrieve-sd-jwt-vc-credential-template.md) | GET | Retrieves an SD-JWT VC credential template from Paradym. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Paradym. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Paradym. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Paradym. |

