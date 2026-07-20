# Picky Assist: Fetch Group Details



```
GET https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/fetch-group-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picky Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/fetch-group-details?connectionId=$CONNECTION_ID&group_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/fetch-group-details?${params}`, {
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
| `group_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "group_admins": [
        {
          "created_time": "string",
          "number": "string"
        }
      ],
      "group_created_date": "string",
      "group_icon_link": "https://example.com",
      "group_id": "string",
      "group_invite_link": "https://example.com",
      "group_members": [
        {
          "created_time": "string",
          "number": "string"
        }
      ],
      "group_subject": "string",
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group_admins[].created_time` | string |  |
| `group_admins[].number` | string |  |
| `group_created_date` | string |  |
| `group_icon_link` | string |  |
| `group_id` | string |  |
| `group_invite_link` | string |  |
| `group_members[].created_time` | string |  |
| `group_members[].number` | string |  |
| `group_subject` | string |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Picky Assist API, this operation is `POST /group-details` (base URL `https://app.pickyassist.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-group-details.md) for the provider-specific parameters and requirements.

