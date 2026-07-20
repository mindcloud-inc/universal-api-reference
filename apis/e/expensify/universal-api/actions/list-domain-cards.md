# Expensify: List Domain Cards

Retrieves domain cards from Expensify.

```
GET https://connect.mindcloud.co/v1/universal/expensify/latest/actions/list-domain-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/list-domain-cards?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expensify/latest/actions/list-domain-cards?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | The domain to list assigned cards for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bank": "string",
      "cardId": "string",
      "cardName": "Ava Chen",
      "cardNumber": "string",
      "created": "string",
      "email": "ava@example.com",
      "externalEmployeeID": "string",
      "lastImport": "string",
      "lastImportResult": 1,
      "reimbursable": true,
      "scrapeMinDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bank` | string |  |
| `cardId` | string |  |
| `cardName` | string |  |
| `cardNumber` | string |  |
| `created` | string |  |
| `email` | string |  |
| `externalEmployeeID` | string |  |
| `lastImport` | string |  |
| `lastImportResult` | number |  |
| `reimbursable` | boolean |  |
| `scrapeMinDate` | string |  |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-domain-cards.md) for the provider-specific parameters and requirements.

