# EzzyCRM: Update Lead Stage



```
PUT https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/update-lead-stage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EzzyCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/update-lead-stage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dealId": 1,
  "dealStageCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/update-lead-stage', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dealId": 1,
    "dealStageCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dealId` | number | yes | ID of the lead. |
| `dealStageCode` | string | yes | Stage code for update of this lead. |

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

Through the native EzzyCRM API, this operation is `POST /api/updateleadstage` (base URL `https://ezzycrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead-stage.md) for the provider-specific parameters and requirements.

