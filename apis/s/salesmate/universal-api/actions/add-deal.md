# Salesmate: Add Deal



```
POST https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/add-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/add-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "owner": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/add-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "owner": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Deal title. |
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
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Salesmate API, this operation is `POST /deal/v4` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-deal.md) for the provider-specific parameters and requirements.

