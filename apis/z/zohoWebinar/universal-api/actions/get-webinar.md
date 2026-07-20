# Zoho Webinar: Get Webinar

Retrieves webinar details from Zoho Webinar.

```
GET https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/get-webinar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Webinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/get-webinar?connectionId=$CONNECTION_ID&organizationId=%7B%7Bcredentials.organizationId%7D%7D&webinarKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "{{credentials.organizationId}}",
  "webinarKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/get-webinar?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "session": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `session` | object |  |

## Native endpoint

Through the native Zoho Webinar API, this operation is `GET /api/v2/:organizationId/webinar/:webinarKey.json` (base URL `https://webinar.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webinar.md) for the provider-specific parameters and requirements.

