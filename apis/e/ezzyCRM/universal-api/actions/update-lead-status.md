# EzzyCRM: Update Lead Status



```
PUT https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/update-lead-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EzzyCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/update-lead-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dealId": 1,
  "dealStatus": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/update-lead-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dealId": 1,
    "dealStatus": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dealId` | number | yes | ID of the lead. |
| `dealStatus` | string | yes | Status for update of this lead. |
| `lostReasonId` | number | no | ID of the reason when lead status is Lost. |
| `comments` | string | no | Comments for the lost lead. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "dealId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `dealId` | number |  |

## Native endpoint

Through the native EzzyCRM API, this operation is `POST /api/updateleadstatus` (base URL `https://ezzycrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead-status.md) for the provider-specific parameters and requirements.

