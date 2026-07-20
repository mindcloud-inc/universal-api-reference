# Ecologi: Get Total Tonnes of CO2e Removed

Retrieves total CO2e removed from Ecologi.

```
GET https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-tonnes-of-co2e-removed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecologi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-tonnes-of-co2e-removed?connectionId=$CONNECTION_ID&username=business-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "business-name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-tonnes-of-co2e-removed?${params}`, {
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
| `username` | string | yes | Your Ecologi username. Example: `business-name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pending": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pending` | number | All unpaid carbon removal for this user. |
| `total` | number | All paid carbon removal for this user. |

## Native endpoint

Through the native Ecologi API, this operation is `GET /users/:username/carbon-removal` (base URL `https://public.ecologi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-total-tonnes-of-co2e-removed.md) for the provider-specific parameters and requirements.

