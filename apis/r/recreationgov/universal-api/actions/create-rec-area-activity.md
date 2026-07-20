# Recreation.gov: Create Rec Area Activity

Creates a recreation area activity in Recreation.gov.

```
POST https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/create-rec-area-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recreation.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/create-rec-area-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": 1,
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/create-rec-area-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": 1,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | number | yes |  |
| `id` | number | yes |  |
| `description` | string | no |  |
| `feeDescription` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "MESSAGE": "string",
      "STATUSCODE": 1,
      "SUCCESS": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `MESSAGE` | string |  |
| `STATUSCODE` | number |  |
| `SUCCESS` | boolean |  |

## Native endpoint

Through the native Recreation.gov API, this operation is `POST /recareas/{id}/activities` (base URL `https://ridb.recreation.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-rec-area-activity.md) for the provider-specific parameters and requirements.

