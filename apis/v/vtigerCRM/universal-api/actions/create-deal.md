# Vtiger CRM: Create Deal

Creates a new deal in Vtiger CRM.

```
POST https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vtiger CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "element": {
    "pipeline": "Pipeline",
    "closingdate": "2026-04-30",
    "sales_stage": "Qualification",
    "potentialname": "Stage3 Default Deal",
    "assigned_user_id": "19x1"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "element": {"pipeline":"Pipeline","closingdate":"2026-04-30","sales_stage":"Qualification","potentialname":"Stage3 Default Deal","assigned_user_id":"19x1"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `element` | string | yes | JSON object string for the Deal fields to create. Default: `{"pipeline":"Pipeline","closingdate":"2026-04-30","sales_stage":"Qualification","potentialname":"Stage3 Default Deal","assigned_user_id":"19x1"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Vtiger Deal id. |
| `label` | string | Deal label. |
| `url` | string | Deal URL in Vtiger. |

## Native endpoint

Through the native Vtiger CRM API, this operation is `POST /create?elementType=Potentials` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

