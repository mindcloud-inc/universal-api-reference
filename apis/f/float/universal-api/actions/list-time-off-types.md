# Float: List Time Off Types

Retrieves time off types from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/list-time-off-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/list-time-off-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/list-time-off-types?${params}`, {
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
| `active` | number | no | Filter only on active or inactive time off types |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "approvalRequired": 1,
      "color": "string",
      "createdBy": 1,
      "groupId": 1,
      "sortOrder": 1,
      "timeoffTypeId": 1,
      "timeoffTypeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `approvalRequired` | number |  |
| `color` | string |  |
| `createdBy` | number |  |
| `groupId` | number |  |
| `sortOrder` | number |  |
| `timeoffTypeId` | number |  |
| `timeoffTypeName` | string |  |

## Native endpoint

Through the native Float API, this operation is `GET /timeoff-types` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-off-types.md) for the provider-specific parameters and requirements.

