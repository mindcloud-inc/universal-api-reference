# Joiin: Update Company

Updates an existing company in Joiin.

```
PUT https://connect.mindcloud.co/v1/universal/joiin/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Joiin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/joiin/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen",
  "sourceSystem": "string",
  "currency": "string",
  "fiscalYearStartMonth": "string",
  "accounts[]": [
    {}
  ],
  "valueFormat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/joiin/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen",
    "sourceSystem": "string",
    "currency": "string",
    "fiscalYearStartMonth": "string",
    "accounts[]": [{}],
    "valueFormat": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Joiin company ID. |
| `name` | string | yes | The company name. |
| `externalId` | string | no | An external identifier for the company. |
| `sourceSystem` | string | yes | The source system for the imported company data. |
| `currency` | string | yes | The company currency code, for example USD. |
| `fiscalYearStartMonth` | string | yes | The month in which the company's fiscal year starts. |
| `ownershipShare` | number | no | The ownership share for the company. |
| `accounts[]` | array<object> | yes | The accounts array to import into Joiin. |
| `valueFormat` | string | yes | The format of the imported account values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string | The Joiin company ID for the updated company. |

## Native endpoint

Through the native Joiin API, this operation is `PUT /v1/companies/:id` (base URL `https://app-api.joiin.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

