# Toofr: Classify Company

Retrieves company classification details from Toofr.

```
GET https://connect.mindcloud.co/v1/universal/toofr/latest/actions/classify-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/classify-company?connectionId=$CONNECTION_ID&companyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toofr/latest/actions/classify-company?${params}`, {
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
| `companyName` | string | yes | Company name to classify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agency": true,
      "category": "string",
      "companyName": "Ava Chen",
      "industry": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agency` | boolean |  |
| `category` | string |  |
| `companyName` | string |  |
| `industry` | string |  |

## Native endpoint

Through the native Toofr API, this operation is `GET /classify` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/classify-company.md) for the provider-specific parameters and requirements.

