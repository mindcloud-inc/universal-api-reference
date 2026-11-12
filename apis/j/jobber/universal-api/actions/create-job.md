# Jobber: Create Job



```
POST https://connect.mindcloud.co/v1/universal/jobber/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jobber/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyId": "string",
  "scheduling": "{\"startAt\":\"2026-07-29T12:00:00Z\"}",
  "invoicing": "{\"schedule\":\"AFTER_COMPLETION\"}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jobber/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyId": "string",
    "scheduling": "{\"startAt\":\"2026-07-29T12:00:00Z\"}",
    "invoicing": "{\"schedule\":\"AFTER_COMPLETION\"}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertyId` | string | yes | Property ID for the new Jobber job. |
| `scheduling` | string | yes | JSON object with JobSchedulingAttributes. Example: `{"startAt":"2026-07-29T12:00:00Z"}`. |
| `invoicing` | string | yes | JSON object with JobInvoicingAttributes. Example: `{"schedule":"AFTER_COMPLETION"}`. |
| `title` | string | no | Optional job title. |
| `customFields` | string | no | Optional JSON array of custom field inputs. Example: `[{"customFieldConfigurationId":"...","valueText":"..."}]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jobber API returns.

## Native endpoint

Through the native Jobber API, this operation is `POST graphql` (base URL `https://api.getjobber.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

