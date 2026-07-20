# Countly: List User Profiles

Retrieves all user profiles from Countly.

```
GET https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-user-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Countly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-user-profiles?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/countly/latest/actions/list-user-profiles?${params}`, {
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
| `appId` | string | yes | Countly app ID to list user profiles for. |
| `iDisplayStart` | number | no | Offset from which to start displaying users. |
| `iDisplayLength` | number | no | Number of users to display from the offset. |
| `sSearch` | string | no | Full-word search on user names or email addresses. |
| `filter` | string | no | User filter, such as user-all, user-known, or user-anonymous. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | no | JSON string encoded MongoDB query for user filtering. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aaData": [
        {}
      ],
      "iTotalDisplayRecords": 1,
      "iTotalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aaData` | array<object> |  |
| `iTotalDisplayRecords` | number |  |
| `iTotalRecords` | number |  |

## Native endpoint

Through the native Countly API, this operation is `GET /o` (base URL `https://mindcloud-fe49f15890040.flex.countly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-profiles.md) for the provider-specific parameters and requirements.

