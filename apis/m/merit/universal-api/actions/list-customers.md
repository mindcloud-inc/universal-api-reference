# Merit: List Customers



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-customers?${params}`, {
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
| `Name` | string | no | Broad-match customer name filter from Merit docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ChangedDate": "2026-05-07T12:00:00.000Z",
      "CountryCode": "string",
      "CustomerId": "string",
      "Email": "ava@example.com",
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ChangedDate` | date |  |
| `CountryCode` | string |  |
| `CustomerId` | string |  |
| `Email` | string |  |
| `Name` | string |  |

## Native endpoint

Through the native Merit API, this operation is `POST v1/getcustomers` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

