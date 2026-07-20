# <img src="https://images.mindcloud.co/apps/icons/updownio_1773864050089.png" alt="updown.io logo" width="28" height="28"> updown.io: Universal API

Monitor websites, manage checks, alert recipients, monitoring nodes, and status pages in updown.io.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/updownio/latest
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://updown.io
- **Vendor API docs:** https://updown.io/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Checks](actions/list-checks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-checks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Check

| Action | Method | Description |
| --- | --- | --- |
| [Create Check](actions/create-check.md) | POST | Creates a new check in updown.io. |
| [Delete Check](actions/delete-check.md) | DELETE | Deletes an existing check from updown.io. |
| [Get Check](actions/get-check.md) | GET | Retrieves a monitoring check from updown.io. |
| [List Checks](actions/list-checks.md) | GET | Retrieves all monitoring checks from updown.io. |
| [Update Check](actions/update-check.md) | PUT | Updates an existing check in updown.io. |

### Check Downtime

| Action | Method | Description |
| --- | --- | --- |
| [List Check Downtimes](actions/list-check-downtimes.md) | GET | Retrieves all check downtimes from updown.io. |

### Check Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Check Metrics](actions/get-check-metrics.md) | GET | Retrieves detailed check metrics from updown.io. |

### Node

| Action | Method | Description |
| --- | --- | --- |
| [List Nodes](actions/list-nodes.md) | GET | Retrieves all monitoring nodes from updown.io. |

### Node Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [List Node IP Addresses](actions/list-node-ip-addresses.md) | GET | Retrieves node IP addresses from updown.io. |

### Node Ipv4 Address

| Action | Method | Description |
| --- | --- | --- |
| [List Node IPv4 Addresses](actions/list-node-ipv4-addresses.md) | GET | Retrieves node IPv4 addresses from updown.io. |

### Node Ipv6 Address

| Action | Method | Description |
| --- | --- | --- |
| [List Node IPv6 Addresses](actions/list-node-ipv6-addresses.md) | GET | Retrieves node IPv6 addresses from updown.io. |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient](actions/create-recipient.md) | POST | Creates a new alert recipient in updown.io. |
| [Delete Recipient](actions/delete-recipient.md) | DELETE | Deletes an alert recipient from updown.io. |
| [List Recipients](actions/list-recipients.md) | GET | Retrieves all alert recipients from updown.io. |

### Status Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Status Page](actions/create-status-page.md) | POST | Creates a new status page in updown.io. |
| [Delete Status Page](actions/delete-status-page.md) | DELETE | Deletes an existing status page from updown.io. |
| [List Status Pages](actions/list-status-pages.md) | GET | Retrieves all status pages from updown.io. |
| [Update Status Page](actions/update-status-page.md) | PUT | Updates an existing status page in updown.io. |

