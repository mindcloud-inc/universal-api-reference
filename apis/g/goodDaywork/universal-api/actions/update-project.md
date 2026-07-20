# GoodDay.work: Update Project

Updates an existing project in GoodDay.work.

```
PUT https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "4uTCIw",
  "userId": "Hn7mvN"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "4uTCIw",
    "userId": "Hn7mvN"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | GoodDay project ID. Default: `4uTCIw`. |
| `userId` | string | yes | User on behalf of whom API executes update. Default: `Hn7mvN`. |
| `progress` | number | no | Project progress percentage 0-100. Default: `30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "id": "string",
      "name": "Ava Chen",
      "ownerUserId": "string",
      "progress": 1,
      "startDate": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string | Project end date. |
| `id` | string | Project ID. |
| `name` | string | Project name. |
| `ownerUserId` | string | Owner user ID. |
| `progress` | number | Project progress percentage. |
| `startDate` | string | Project start date. |
| `status` | string | Project status label. |

## Native endpoint

Through the native GoodDay.work API, this operation is `PUT /project/:projectId` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

