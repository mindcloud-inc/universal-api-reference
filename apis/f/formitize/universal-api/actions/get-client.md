# Formitize: Get Client

Retrieves a client from Formitize.

```
GET https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-client?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formitize/latest/actions/get-client?${params}`, {
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
| `clientId` | string | no | Formitize client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingName": "Ava Chen",
      "contact": [
        {}
      ],
      "id": "string",
      "location": [
        {}
      ],
      "primaryAddress": "string",
      "primaryAddressID": "string",
      "primaryContactEmail": "ava@example.com",
      "primaryContactID": "string",
      "primaryContactName": "Ava Chen",
      "primaryContactPhone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingName` | string |  |
| `contact` | array<object> |  |
| `id` | string |  |
| `location` | array<object> |  |
| `primaryAddress` | string |  |
| `primaryAddressID` | string |  |
| `primaryContactEmail` | string |  |
| `primaryContactID` | string |  |
| `primaryContactName` | string |  |
| `primaryContactPhone` | string |  |

## Native endpoint

Through the native Formitize API, this operation is `GET /crm/client/:clientID` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

