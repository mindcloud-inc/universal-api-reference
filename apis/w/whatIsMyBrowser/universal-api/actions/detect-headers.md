# WhatIsMyBrowser: Detect Headers

Retrieves browser and device details from WhatIsMyBrowser using request headers.

```
GET https://connect.mindcloud.co/v1/universal/whatIsMyBrowser/latest/actions/detect-headers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatIsMyBrowser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatIsMyBrowser/latest/actions/detect-headers?connectionId=$CONNECTION_ID&headers%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "headers[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatIsMyBrowser/latest/actions/detect-headers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `headers[]` | array<object> | yes | Ordered list of visitor HTTP headers. Each item should include name and value fields, preserving the order received by your server. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detection": {
        "hardware_sub_sub_type": "string",
        "hardware_sub_type": "string",
        "hardware_type": "string",
        "layout_engine_name": "Ava Chen",
        "operating_system": "string",
        "operating_system_flavour": "string",
        "operating_system_name": "Ava Chen",
        "operating_system_name_code": "Ava Chen",
        "operating_system_version": "string",
        "operating_system_version_full": [
          "string"
        ],
        "simple_operating_platform_string": "string",
        "simple_software_string": "string",
        "simple_sub_description_string": "string",
        "software": "string",
        "software_name": "Ava Chen",
        "software_name_code": "Ava Chen",
        "software_sub_type": "string",
        "software_type": "string",
        "software_version": "string",
        "software_version_full": [
          "string"
        ],
        "software_version_full_age_days": 1,
        "software_version_full_release_date": "2026-05-07T12:00:00.000Z"
      },
      "result": {
        "code": "string",
        "message": "string",
        "message_code": "string"
      },
      "risks": {},
      "version_check": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detection` | object | Browser and device detection details returned for the supplied request headers. |
| `detection.hardware_sub_sub_type` | string | Detected detailed hardware subtype when returned by the plan. |
| `detection.hardware_sub_type` | string | Detected hardware subtype when returned by the plan. |
| `detection.hardware_type` | string | Detected hardware type when returned by the plan. |
| `detection.layout_engine_name` | string | Detected browser layout engine when returned by the plan. |
| `detection.operating_system` | string | Detected operating system summary. |
| `detection.operating_system_flavour` | string | Operating system flavour when available. |
| `detection.operating_system_name` | string | Detected operating system name. |
| `detection.operating_system_name_code` | string | Provider code for the detected operating system. |
| `detection.operating_system_version` | string | Detected operating system version. |
| `detection.operating_system_version_full` | array<string> | Detected full operating system version components. |
| `detection.simple_operating_platform_string` | string | Simplified operating platform description when available. |
| `detection.simple_software_string` | string | Human-readable browser and operating system summary. |
| `detection.simple_sub_description_string` | string | Additional simplified browser/device description when available. |
| `detection.software` | string | Detected browser/software name and major version. |
| `detection.software_name` | string | Detected browser/software name. |
| `detection.software_name_code` | string | Provider code for the detected software name. |
| `detection.software_sub_type` | string | Detected software subcategory when returned by the plan. |
| `detection.software_type` | string | Detected software category when returned by the plan. |
| `detection.software_version` | string | Detected software major version. |
| `detection.software_version_full` | array<string> | Detected full software version components. |
| `detection.software_version_full_age_days` | number | Age in days for the full software version when the plan includes version checking. |
| `detection.software_version_full_release_date` | date | Release date for the full software version when the plan includes version checking. |
| `result` | object | Provider result metadata. |
| `result.code` | string | High-level provider result code. |
| `result.message` | string | Provider result message. |
| `result.message_code` | string | Provider-specific result message code. |
| `risks` | object | User agent and client hints risk analysis when available for the account plan. |
| `version_check` | object | Version freshness details when available for the account plan. |

## Native endpoint

Through the native WhatIsMyBrowser API, this operation is `POST /detect` (base URL `https://api.whatismybrowser.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-headers.md) for the provider-specific parameters and requirements.

