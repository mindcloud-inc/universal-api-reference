# MyOwnConference: List webinars

Retrieves scheduled webinars from MyOwnConference.

```
GET https://connect.mindcloud.co/v1/universal/myOwnConference/latest/actions/list-webinars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyOwnConference `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myOwnConference/latest/actions/list-webinars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myOwnConference/latest/actions/list-webinars?${params}`, {
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
      "alias": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "language": "string",
      "name": "Ava Chen",
      "start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | Unique webinar alias. |
| `created` | date | Creation timestamp. |
| `description` | string | Webinar description or agenda. |
| `duration` | number | Planned duration in minutes when present. |
| `language` | string | Webinar language. |
| `name` | string | Webinar title. |
| `start` | date | Scheduled start timestamp. |

## Native endpoint

Through the native MyOwnConference API, this operation is `POST /` (base URL `https://api.mywebinar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webinars.md) for the provider-specific parameters and requirements.

