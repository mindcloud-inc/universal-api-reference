# <img src="https://images.mindcloud.co/apps/icons/images_1775591521780.png" alt="Novofon logo" width="28" height="28"> Novofon: Universal API

Novofon provides virtual PBX, SIP, callback, call statistics, call recordings, and direct-number operations for business telephony workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/novofon/latest
- **Category:** Support / Contact Center
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.novofon.com
- **Vendor API docs:** https://novofon.com/instructions/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Billing

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves account balance from Novofon. |

### Call Requests

| Action | Method | Description |
| --- | --- | --- |
| [Request Callback](actions/request-callback.md) | POST | Creates a callback request in Novofon. |
| [Request Check Number](actions/request-check-number.md) | POST | Creates a number check request in Novofon. |

### Direct Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Get Direct Number](actions/get-direct-number.md) | GET | Retrieves a direct number from Novofon. |
| [List Direct Number Countries](actions/list-direct-number-countries.md) | GET | Retrieves direct number countries from Novofon. |
| [List Direct Numbers](actions/list-direct-numbers.md) | GET | Retrieves direct numbers from Novofon. |

### Pbx

| Action | Method | Description |
| --- | --- | --- |
| [Get PBX Internal Status](actions/get-pbx-internal-status.md) | GET | Retrieves PBX internal status from Novofon. |
| [List PBX Internal Numbers](actions/list-pbx-internal-numbers.md) | GET | Retrieves PBX internal numbers from Novofon. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Request Call Recording](actions/request-call-recording.md) | GET | Retrieves call recording links from Novofon. |

### Sip

| Action | Method | Description |
| --- | --- | --- |
| [Get SIP Status](actions/get-sip-status.md) | GET | Retrieves SIP status from Novofon. |
| [List SIP Numbers](actions/list-sip-numbers.md) | GET | Retrieves SIP numbers from Novofon. |

### Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Statistics](actions/get-call-statistics.md) | GET | Retrieves call statistics from Novofon. |
| [Get Callback Widget Statistics](actions/get-callback-widget-statistics.md) | GET | Retrieves callback widget statistics from Novofon. |
| [Get Incoming Call Statistics](actions/get-incoming-call-statistics.md) | GET | Retrieves incoming call statistics from Novofon. |
| [Get PBX Call Statistics](actions/get-pbx-call-statistics.md) | GET | Retrieves PBX call statistics from Novofon. |

### System

| Action | Method | Description |
| --- | --- | --- |
| [Get Timezone](actions/get-timezone.md) | GET | Retrieves account timezone details from Novofon. |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves supported currencies from Novofon. |
| [List Languages](actions/list-languages.md) | GET | Retrieves supported languages from Novofon. |

