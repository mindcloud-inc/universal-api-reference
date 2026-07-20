# Pilvio: List Billing Account Resources



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-billing-account-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-billing-account-resources?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-billing-account-resources?${params}`, {
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
| `id` | string | yes | Billing account ID whose resources should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backup": true,
      "billingAccount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "hostname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backup` | boolean |  |
| `billingAccount` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `hostname` | string |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /user-resource/billing_resources` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-billing-account-resources.md) for the provider-specific parameters and requirements.

