# Zoho Webinar: List Users

Retrieves users from Zoho Webinar.

```
GET https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Webinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/list-users?connectionId=$CONNECTION_ID&organizationId=%7B%7Bcredentials.organizationId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "{{credentials.organizationId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/list-users?${params}`, {
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
| `index` | number | no |  |
| `count` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "representation": [
        {}
      ],
      "resourceType": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `representation` | array<object> |  |
| `resourceType` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Zoho Webinar API, this operation is `GET /api/v2/:organizationId/user` (base URL `https://webinar.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

