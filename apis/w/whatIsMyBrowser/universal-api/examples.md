# WhatIsMyBrowser Universal API Examples

These examples use the MindCloud API key and WhatIsMyBrowser connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Version Numbers

Retrieves tracked software version numbers from WhatIsMyBrowser.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatIsMyBrowser/latest/actions/get-version-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatIsMyBrowser/latest/actions/get-version-numbers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "download_url": "https://example.com",
      "latest_version": {
        "build": "string",
        "platform_version": [
          "string"
        ],
        "release_date": "2026-05-07T12:00:00.000Z",
        "update": "string",
        "version_number": [
          "string"
        ]
      },
      "result": {
        "code": "string",
        "message": "string",
        "message_code": "string"
      },
      "update_url": "https://example.com",
      "version_data": {
        "operating-system": {},
        "plugin": {},
        "software": {}
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Version Numbers action reference](actions/get-version-numbers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/whatIsMyBrowser/latest/actions/get-version-numbers).
