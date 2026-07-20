# Salesmate: Update Deal



```
PUT https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dealId": 1,
  "owner": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dealId": 1,
    "owner": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dealId` | number | yes | Salesmate deal ID. |
| `title` | string | no | Deal title. |
| `owner` | number | yes | Salesmate user ID that owns the deal. |
| `primaryContact` | number | no | Primary contact linked to the deal. |
| `primaryCompany` | number | no | Primary company linked to the deal. |
| `dealValue` | number | no | Deal value amount. |
| `estimatedCloseDate` | date | no | Estimated close date/time. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pipeline` | string | no | Pipeline name. |
| `stage` | string | no | Pipeline stage. |
| `status` | string | no | Deal status. |
| `priority` | string | no | Deal priority. |
| `source` | string | no | Deal source. |
| `description` | string | no | Internal deal description. |
| `tags` | string | no | Comma-separated tag list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Salesmate API, this operation is `PUT /deal/v4/:dealId` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal.md) for the provider-specific parameters and requirements.

