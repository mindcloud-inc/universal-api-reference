# Xperiencify: Redeem Student Points

Redeems student points in Xperiencify.

```
PUT https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/redeem-student-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/redeem-student-points" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "courseIds[]": [
    1
  ],
  "studentIds[]": [
    1
  ],
  "pointsType": "string",
  "value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/redeem-student-points', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "courseIds[]": [1],
    "studentIds[]": [1],
    "pointsType": "string",
    "value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courseIds[]` | array<number> | yes | One or more course IDs. |
| `studentIds[]` | array<number> | yes | One or more student IDs. |
| `pointsType` | string | yes | Use xp, xxp, or bp. |
| `value` | number | yes | Positive number of points. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Xperiencify API returns.

## Native endpoint

Through the native Xperiencify API, this operation is `POST /api/public/student/redeem_points/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/redeem-student-points.md) for the provider-specific parameters and requirements.

