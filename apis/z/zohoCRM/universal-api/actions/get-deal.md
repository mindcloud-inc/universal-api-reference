# Zoho CRM: Get Deal

Retrieves a deal record from Zoho CRM.

```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-deal?connectionId=$CONNECTION_ID&ids=string&fields=id%2CDeal_Name%2CStage%2CAmount" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string",
  "fields": "id,Deal_Name,Stage,Amount"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-deal?${params}`, {
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
| `ids` | string | yes | The Zoho CRM record ID to retrieve. |
| `fields` | string | yes | Comma-separated Zoho CRM field API names to include in the response. Default: `id,Deal_Name,Stage,Amount`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "dealName": "Ava Chen",
      "id": "string",
      "stage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `dealName` | string |  |
| `id` | string |  |
| `stage` | string |  |

## Native endpoint

Through the native Zoho CRM API, this operation is `GET /Deals` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

