# Cloud BOT: List Contracts

Retrieves contracts from Cloud BOT.

```
GET https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud BOT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-contracts?${params}`, {
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
| `properties` | string | no | Comma-separated list of additional contract properties to include, such as plan or owner. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "code": 1,
      "department": "string",
      "location": "string",
      "name": "Ava Chen",
      "organization": "string",
      "owner": "string",
      "phone": "string",
      "plan": "string",
      "postcode": "string",
      "publicId": "string",
      "publicPath": "string",
      "timezone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Address |
| `code` | number | Response status code |
| `department` | string | Department |
| `location` | string | Contract location |
| `name` | string | Contract name |
| `organization` | string | Organization name |
| `owner` | string | Plan owner email |
| `phone` | string | Phone number |
| `plan` | string | Plan name |
| `postcode` | string | Postal code |
| `publicId` | string | Contract public ID |
| `publicPath` | string | Contract public path |
| `timezone` | string | Contract time zone |
| `username` | string | Contact person |

## Native endpoint

Through the native Cloud BOT API, this operation is `GET /services/contracts` (base URL `https://api.c-bot.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contracts.md) for the provider-specific parameters and requirements.

