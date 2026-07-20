# InflatableOffice: List Detailed Customers

Retrieves customers with detailed fields from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-detailed-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-detailed-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-detailed-customers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "cellphone": "string",
      "city": "string",
      "country": "string",
      "createtimeUtc": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "fromCustomerProvider": true,
      "href": "string",
      "id": "string",
      "lastname": "Chen",
      "modifiedtimeUtc": "string",
      "organization": "string",
      "requestTime": 1,
      "state": "string",
      "street": "string",
      "tags": [
        "string"
      ],
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cellphone` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createtimeUtc` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `fromCustomerProvider` | boolean |  |
| `href` | string |  |
| `id` | string |  |
| `lastname` | string |  |
| `modifiedtimeUtc` | string |  |
| `organization` | string |  |
| `requestTime` | number |  |
| `state` | string |  |
| `street` | string |  |
| `tags` | array<string> |  |
| `zip` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /customers` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-detailed-customers.md) for the provider-specific parameters and requirements.

