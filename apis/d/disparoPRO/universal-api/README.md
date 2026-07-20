# <img src="https://images.mindcloud.co/apps/icons/favicon-disparo-pro-2025_1775073502019.png" alt="Disparo PRO logo" width="28" height="28"> Disparo PRO: Universal API

Disparo PRO provides an RCS API for creating message templates and sending verified RCS messages through the Disparo Pro platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/disparoPRO/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://disparopro.com.br/
- **Vendor API docs:** https://painel.disparopro.com.br/docs/rcs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Basic RCS Message](actions/send-basic-rcs-message.md) | POST | Creates a basic RCS message in Disparo PRO. |
| [Send Single RCS Message](actions/send-single-rcs-message.md) | POST | Creates a single RCS message in Disparo PRO. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Activate Template](actions/activate-template.md) | PUT | Updates a template to active in Disparo PRO. |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Disparo PRO. |
| [Deactivate Template](actions/deactivate-template.md) | PUT | Updates a template to inactive in Disparo PRO. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Disparo PRO. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Disparo PRO. |

