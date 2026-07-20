# TeamUp: Get Calendar Configuration

Retrieves configuration for a TeamUp calendar.

```
GET https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-calendar-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-calendar-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamUp/latest/actions/get-calendar-configuration?${params}`, {
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
      "configuration": {
        "identity": {
          "title": "string"
        },
        "link": {
          "key": "https://example.com"
        },
        "subcalendars": [
          [
            {}
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | object |  |
| `configuration.identity` | object |  |
| `configuration.identity.title` | string |  |
| `configuration.link` | object |  |
| `configuration.link.key` | string |  |
| `configuration.subcalendars[]` | array<object> |  |
| `configuration.subcalendars[].id` | number |  |
| `configuration.subcalendars[].name` | string |  |

## Native endpoint

Through the native TeamUp API, this operation is `GET /:calendarKeyOrId/configuration` (base URL `https://api.teamup.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calendar-configuration.md) for the provider-specific parameters and requirements.

