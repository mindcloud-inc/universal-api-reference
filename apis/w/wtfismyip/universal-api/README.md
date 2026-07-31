# <img src="https://images.mindcloud.co/apps/icons/wtfismyip_1785420607279.png" alt="wtfismyip logo" width="28" height="28"> wtfismyip: Universal API

View the public IP and network context seen by the wtfismyip request runner.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wtfismyip/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wtfismyip.com/
- **Vendor API docs:** https://wtfismyip.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Runner IP as Text](actions/get-runner-ip-as-text.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wtfismyip/latest/actions/get-runner-ip-as-text?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Runner IP as Text](actions/get-runner-ip-as-text.md) | GET |  |

### Ip Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Runner IP Information](actions/get-runner-ip-information.md) | GET |  |
| [Get Runner IP Information as XML](actions/get-runner-ip-information-as-xml.md) | GET |  |
| [Get Runner IP Information as YAML](actions/get-runner-ip-information-as-yaml.md) | GET |  |

