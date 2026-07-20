# <img src="https://images.mindcloud.co/apps/icons/buy-me-acoffee_1773710469516.png" alt="Buy Me a Coffee logo" width="28" height="28"> Buy Me a Coffee: Universal API

Read your Buy Me a Coffee memberships, supporters, and extras purchases using a personal access token.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/buyMeACoffee/latest
- **Category:** Commerce
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://buymeacoffee.com
- **Vendor API docs:** https://developers.buymeacoffee.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Onetime Supporters](actions/list-onetime-supporters.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-onetime-supporters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Extras Purchases

| Action | Method | Description |
| --- | --- | --- |
| [Get Extra Purchase](actions/get-extra-purchase.md) | GET | Retrieves an extra purchase from Buy Me a Coffee by purchase ID. |
| [List Extra Purchases](actions/list-extra-purchases.md) | GET | Retrieves extra purchases from Buy Me a Coffee. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Get Member](actions/get-member.md) | GET | Retrieves a member from Buy Me a Coffee by membership ID. |
| [List Members](actions/list-members.md) | GET | Retrieves members from Buy Me a Coffee. |

### Supporters

| Action | Method | Description |
| --- | --- | --- |
| [Get Onetime Supporter](actions/get-onetime-supporter.md) | GET | Retrieves one-time supporter details from Buy Me a Coffee by supporter ID. |
| [List Onetime Supporters](actions/list-onetime-supporters.md) | GET | Retrieves onetime supporters from Buy Me a Coffee. |

