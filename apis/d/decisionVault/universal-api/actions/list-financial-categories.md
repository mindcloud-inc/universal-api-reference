# DecisionVault: List Financial Categories

Retrieves financial categories available in DecisionVault.

```
GET https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-financial-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DecisionVault `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-financial-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-financial-categories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "ask_beneficiaries": true,
      "ask_credit_value": true,
      "ask_debit_value": true,
      "for_questionnaire": "string",
      "general_category": {},
      "id": "string",
      "order": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `ask_beneficiaries` | boolean |  |
| `ask_credit_value` | boolean |  |
| `ask_debit_value` | boolean |  |
| `for_questionnaire` | string |  |
| `general_category` | object |  |
| `id` | string |  |
| `order` | number |  |
| `title` | string |  |

## Native endpoint

Through the native DecisionVault API, this operation is `GET /financial-categories` (base URL `https://api.decisionvault.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-financial-categories.md) for the provider-specific parameters and requirements.

