# <img src="https://images.mindcloud.co/apps/icons/wimb-icon_1777583413109.png" alt="WhatIsMyBrowser logo" width="28" height="28"> WhatIsMyBrowser: Universal API

WhatIsMyBrowser identifies browsers, operating systems, devices, software versions, and request risks from visitor HTTP headers using the WhatIsMyBrowser API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whatIsMyBrowser/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.whatismybrowser.com/
- **Vendor API docs:** https://developers.whatismybrowser.com/api/docs/v3/integration-guide/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Version Numbers](actions/get-version-numbers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatIsMyBrowser/latest/actions/get-version-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Detected Browser Profile

| Action | Method | Description |
| --- | --- | --- |
| [Detect Headers](actions/detect-headers.md) | GET | Retrieves browser and device details from WhatIsMyBrowser using request headers. |

### Tracked Software Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Version Numbers](actions/get-version-numbers.md) | GET | Retrieves tracked software version numbers from WhatIsMyBrowser. |

