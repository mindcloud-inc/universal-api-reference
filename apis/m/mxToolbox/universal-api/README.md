# <img src="https://images.mindcloud.co/apps/icons/mx-toolbox_1776088834427.png" alt="Mx Toolbox logo" width="28" height="28"> Mx Toolbox: Universal API

Check DNS, MX, and email delivery health with MxToolbox

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mxToolbox/latest
- **Category:** Communication / Email Communications
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mxtoolbox.com/
- **Vendor API docs:** https://knowledgebase.mxtoolbox.com/home/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Blocklist](actions/check-blocklist.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mxToolbox/latest/actions/check-blocklist?connectionId=$CONNECTION_ID&target=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### A Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup A Record](actions/lookup-a-record.md) | GET |  |

### Aaaa Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup AAAA Record](actions/lookup-aaaa-record.md) | GET |  |

### Asn Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup ASN Information](actions/lookup-asn-information.md) | GET |  |

### Bimi Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup BIMI Record](actions/lookup-bimi-record.md) | GET |  |

### Blocklist Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Check Blocklist](actions/check-blocklist.md) | GET |  |

### Cname Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup CNAME Record](actions/lookup-cname-record.md) | GET |  |

### Dkim Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup DKIM Record](actions/lookup-dkim-record.md) | GET |  |

### Dmarc Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup DMARC Record](actions/lookup-dmarc-record.md) | GET |  |

### Dns Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Check DNS Servers](actions/check-dns-servers.md) | GET |  |

### Http Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup HTTP](actions/lookup-http.md) | GET |  |

### Https Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup HTTPS](actions/lookup-https.md) | GET |  |

### Mta-sts Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup MTA-STS Record](actions/lookup-mta-sts-record.md) | GET |  |

### Mx Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup MX Records](actions/lookup-mx-records.md) | GET |  |

### Ptr Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup PTR Record](actions/lookup-ptr-record.md) | GET |  |

### Smtp Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Test SMTP](actions/test-smtp.md) | GET |  |

### Soa Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup SOA Record](actions/lookup-soa-record.md) | GET |  |

### Spf Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup SPF Record](actions/lookup-spf-record.md) | GET |  |

### Tcp Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup TCP Port](actions/lookup-tcp-port.md) | GET |  |

### Txt Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup TXT Record](actions/lookup-txt-record.md) | GET |  |

### Whois Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup WHOIS](actions/lookup-whois.md) | GET |  |

