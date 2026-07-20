# leadtributor.cloud: Update Lead

Updates an existing lead in leadtributor.cloud.

```
PUT https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a leadtributor.cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadtributorcloud/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | yes | ID of the lead to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Empty response body for a successful lead update. |

## Native endpoint

Through the native leadtributor.cloud API, this operation is `PATCH /leads/:leadId` (base URL `https://api.leadtributor.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

