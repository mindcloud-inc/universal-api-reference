# WhatIsMyBrowser: Get Version Numbers

Retrieves tracked software version numbers from WhatIsMyBrowser.

```
GET https://connect.mindcloud.co/v1/universal/whatIsMyBrowser/latest/actions/get-version-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatIsMyBrowser `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_url` | string | Provider download URL for the package when available. |
| `latest_version` | object | Latest version details for a package stream. |
| `latest_version.build` | string | Build identifier when the package uses one. |
| `latest_version.platform_version` | array<string> | Platform version components when returned for the package. |
| `latest_version.release_date` | date | Release date for the latest version when available. |
| `latest_version.update` | string | Additional update number when the package uses one. |
| `latest_version.version_number` | array<string> | Latest version number split into version components. |
| `result` | object | Provider result metadata. |
| `result.code` | string | High-level provider result code. |
| `result.message` | string | Provider result message. |
| `result.message_code` | string | Provider-specific result message code. |
| `update_url` | string | Provider update URL for the package when available. |
| `version_data` | object | Version catalog grouped by software, operating system, and plugin package streams. |
| `version_data.operating-system` | object | Tracked operating system version groups. |
| `version_data.plugin` | object | Tracked browser plugin version groups. |
| `version_data.software` | object | Tracked browser and software version groups. |

## Native endpoint

Through the native WhatIsMyBrowser API, this operation is `GET /version_numbers` (base URL `https://api.whatismybrowser.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-version-numbers.md) for the provider-specific parameters and requirements.

