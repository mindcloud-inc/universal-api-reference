# DecisionVault: List Assets for Matter

Retrieves assets for a matter in DecisionVault.

```
GET https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-assets-for-matter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DecisionVault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-assets-for-matter?connectionId=$CONNECTION_ID&matterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "matterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-assets-for-matter?${params}`, {
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
| `matterId` | string | yes | The matter ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additional_fields": [
        {}
      ],
      "beneficiaries": [
        {}
      ],
      "credit_label": "string",
      "credit_value": "string",
      "debit_label": "string",
      "debit_value": "string",
      "for_fin_category": "string",
      "for_matter": "string",
      "general_category": {},
      "id": "string",
      "identifier_label": "string",
      "identifier_value": "string",
      "net_value": "string",
      "owner_label": "string",
      "owner_value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additional_fields` | array<object> |  |
| `beneficiaries` | array<object> |  |
| `credit_label` | string |  |
| `credit_value` | string |  |
| `debit_label` | string |  |
| `debit_value` | string |  |
| `for_fin_category` | string |  |
| `for_matter` | string |  |
| `general_category` | object |  |
| `id` | string |  |
| `identifier_label` | string |  |
| `identifier_value` | string |  |
| `net_value` | string |  |
| `owner_label` | string |  |
| `owner_value` | string |  |

## Native endpoint

Through the native DecisionVault API, this operation is `GET /matters/:matter_id/assets` (base URL `https://api.decisionvault.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assets-for-matter.md) for the provider-specific parameters and requirements.

