# Zoho Recruit: List Custom Views

Retrieves custom views from Zoho Recruit.

```
GET https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-custom-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Recruit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-custom-views?connectionId=$CONNECTION_ID&moduleApiName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moduleApiName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoRecruit/latest/actions/list-custom-views?${params}`, {
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
| `moduleApiName` | string | yes | The Zoho Recruit module API name whose custom views you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customViews": [
        {}
      ],
      "info": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customViews` | array<object> |  |
| `info` | object |  |

## Native endpoint

Through the native Zoho Recruit API, this operation is `GET /settings/custom_views` (base URL `https://recruit.zoho.com/recruit/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-views.md) for the provider-specific parameters and requirements.

