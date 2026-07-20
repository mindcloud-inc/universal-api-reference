# Vtiger CRM: Create Lead

Creates a new lead in Vtiger CRM.

```
POST https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vtiger CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "element": {
    "company": "MindCloud",
    "lastname": "Default Lead",
    "firstname": "Stage3"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "element": {"company":"MindCloud","lastname":"Default Lead","firstname":"Stage3"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `element` | string | yes | JSON object string for the Lead fields to create. Default: `{"company":"MindCloud","lastname":"Default Lead","firstname":"Stage3"}`. |

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
| `id` | string | Vtiger Lead id. |
| `label` | string | Lead label. |
| `url` | string | Lead URL in Vtiger. |

## Native endpoint

Through the native Vtiger CRM API, this operation is `POST /create?elementType=Leads` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

