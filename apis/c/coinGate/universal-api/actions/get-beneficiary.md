# CoinGate: Get Beneficiary

Retrieves a beneficiary from CoinGate by ID.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-beneficiary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-beneficiary?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-beneficiary?${params}`, {
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
| `id` | string | yes | CoinGate beneficiary ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "beneficiaryType": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "surname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `beneficiaryType` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `surname` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `GET /beneficiaries/:id` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-beneficiary.md) for the provider-specific parameters and requirements.

