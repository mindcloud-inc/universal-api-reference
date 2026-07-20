# PredictLeads: Follow Company

Follows a company in the PredictLeads API.

```
POST https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/follow-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PredictLeads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/follow-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyIdOrDomain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/follow-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyIdOrDomain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyIdOrDomain` | string | yes | Company ID or domain. |
| `customCompanyIdentifier` | string | no | Use your custom company identifier if you want it stored with the follow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": {
        "message": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success.message` | string | Confirmation message for the followed company. |
| `success.type` | string | Success response type. |

## Native endpoint

Through the native PredictLeads API, this operation is `POST /companies/:company_id_or_domain/follow` (base URL `https://predictleads.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/follow-company.md) for the provider-specific parameters and requirements.

