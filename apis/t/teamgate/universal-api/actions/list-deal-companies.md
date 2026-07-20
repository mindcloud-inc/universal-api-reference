# Teamgate: List Deal Companies

Retrieves companies for a deal in Teamgate.

```
GET https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-deal-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-deal-companies?connectionId=$CONNECTION_ID&dealId=79" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dealId": "79"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-deal-companies?${params}`, {
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
| `dealId` | string | yes | Deal ID whose linked companies should be listed. Example: `79`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "isDeleted": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isDeleted` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Teamgate API, this operation is `GET /deals/:deal_id/companies` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deal-companies.md) for the provider-specific parameters and requirements.

