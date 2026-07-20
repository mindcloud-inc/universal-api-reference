# <img src="https://images.mindcloud.co/apps/icons/t-riggercmd_1775822725359.png" alt="TRIGGERcmd logo" width="28" height="28"> TRIGGERcmd: Universal API

Run commands remotely on your computers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tRIGGERcmd/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.triggercmd.com/en/
- **Vendor API docs:** https://docs.triggercmd.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Commands](actions/list-commands.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tRIGGERcmd/latest/actions/list-commands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Command

| Action | Method | Description |
| --- | --- | --- |
| [List Commands](actions/list-commands.md) | GET | Retrieves a list of commands from TRIGGERcmd. |
| [Trigger Command](actions/trigger-command.md) | POST | Triggers a command on a computer in TRIGGERcmd. |

