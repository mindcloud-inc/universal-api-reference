# SmartReach: List Email Settings

Retrieves email settings from SmartReach.

```
GET https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-email-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-email-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-email-settings?${params}`, {
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
| `olderThan` | number | no | timestamp in unix epoch milliseconds |
| `newerThan` | number | no | timestamp in unix epoch milliseconds |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email_settings": [
        {
          "email": "ava@example.com",
          "id": "ava@example.com",
          "service_provider": "ava@example.com"
        }
      ],
      "links": {
        "next": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email_settings[].email` | string |  |
| `email_settings[].id` | string |  |
| `email_settings[].service_provider` | string |  |
| `links.next` | string |  |

## Native endpoint

Through the native SmartReach API, this operation is `GET /email_settings` (base URL `https://api.smartreach.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-settings.md) for the provider-specific parameters and requirements.

