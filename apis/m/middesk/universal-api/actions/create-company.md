# Middesk: Create a company

Creates a company in your Middesk account.

```
POST https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "legalName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "legalName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `legalName` | string | yes | Legal name of the company to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "dbaName": "Ava Chen",
      "externalId": "string",
      "id": "string",
      "legalName": "Ava Chen",
      "object": "string",
      "parentAccount": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `dbaName` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `legalName` | string |  |
| `object` | string |  |
| `parentAccount` | object |  |

## Native endpoint

Through the native Middesk API, this operation is `POST /partner/companies` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

