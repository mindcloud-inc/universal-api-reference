# Countly: Get App Details

Retrieves application details from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-app-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-app-details?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/get-app-details?${params}`, {
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
| `appId` | string | yes | Countly app ID to fetch details for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": [
        [
          {}
        ]
      ],
      "app": {
        "created_at": 1,
        "edited_at": 1,
        "last_data_users": 1,
        "owner": "string",
        "owner_id": "string"
      },
      "global_admin": [
        [
          {}
        ]
      ],
      "user": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin[]` | array<object> |  |
| `app.created_at` | number |  |
| `app.edited_at` | number |  |
| `app.last_data_users` | number |  |
| `app.owner` | string |  |
| `app.owner_id` | string |  |
| `global_admin[]` | array<object> |  |
| `user[]` | array<object> |  |

## Native endpoint

Through the native Countly API, this operation is `GET /o/apps/details` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-details.md) for the provider-specific parameters and requirements.

