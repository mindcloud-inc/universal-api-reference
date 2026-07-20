# UbiBot: List Supported Timezones

Retrieves supported platform timezones from UbiBot.

```
GET https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-supported-timezones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UbiBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-supported-timezones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiBot/latest/actions/list-supported-timezones?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Timezone identifier supported by UbiBot. |
| `name` | string | Timezone display name. |

## Native endpoint

Through the native UbiBot API, this operation is `GET /constants/timezones` (base URL `https://webapi.ubibot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-timezones.md) for the provider-specific parameters and requirements.

