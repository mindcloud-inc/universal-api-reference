# Zoho Webinar: Get Webinar Attendee Report

Retrieves webinar attendee report entries from Zoho Webinar.

```
GET https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/get-webinar-attendee-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Webinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/get-webinar-attendee-report?connectionId=$CONNECTION_ID&organizationId=%7B%7Bcredentials.organizationId%7D%7D&webinarKey=string&index=1&count=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "{{credentials.organizationId}}",
  "webinarKey": "string",
  "index": "1",
  "count": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/get-webinar-attendee-report?${params}`, {
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
| `organizationId` | string | yes | Default: `{{credentials.organizationId}}`. |
| `webinarKey` | string | yes |  |
| `index` | number | yes |  |
| `count` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendeeData": [
        {}
      ],
      "attendeesCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendeeData` | array<object> |  |
| `attendeesCount` | number |  |

## Native endpoint

Through the native Zoho Webinar API, this operation is `GET /api/v2/:organizationId/attendee/:webinarKey.json` (base URL `https://webinar.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webinar-attendee-report.md) for the provider-specific parameters and requirements.

