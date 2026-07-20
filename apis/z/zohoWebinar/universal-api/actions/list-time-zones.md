# Zoho Webinar: List Time Zones

Retrieves time zones from Zoho Webinar.

```
GET https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/list-time-zones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Webinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/list-time-zones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/list-time-zones?${params}`, {
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
| `languageCode` | string | no | Default: `en_US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "offset": "string",
      "timeZone": "string",
      "timeZoneFullName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `offset` | string |  |
| `timeZone` | string |  |
| `timeZoneFullName` | string |  |

## Native endpoint

Through the native Zoho Webinar API, this operation is `GET /api/v2/timezone` (base URL `https://webinar.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-zones.md) for the provider-specific parameters and requirements.

