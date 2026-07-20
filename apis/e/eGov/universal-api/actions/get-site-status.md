# e-Gov: Get Site Status

Retrieves site status from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-site-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-site-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-site-status?${params}`, {
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
      "ckan_version": "string",
      "error_emails_to": "ava@example.com",
      "extensions": [
        "string"
      ],
      "locale_default": "string",
      "site_description": "string",
      "site_title": "string",
      "site_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ckan_version` | string |  |
| `error_emails_to` | string |  |
| `extensions` | array<string> |  |
| `locale_default` | string |  |
| `site_description` | string |  |
| `site_title` | string |  |
| `site_url` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /status_show` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-status.md) for the provider-specific parameters and requirements.

