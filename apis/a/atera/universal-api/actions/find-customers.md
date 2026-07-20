# Atera: Find customers

Finds customers in Atera.

```
GET https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atera/latest/actions/find-customers?${params}`, {
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
      "Country": "string",
      "CreatedOn": "string",
      "CustomerID": 1,
      "CustomerName": "Ava Chen",
      "LastModified": "string",
      "Latitude": 1,
      "Longitude": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Country` | string |  |
| `CreatedOn` | string |  |
| `CustomerID` | number |  |
| `CustomerName` | string |  |
| `LastModified` | string |  |
| `Latitude` | number |  |
| `Longitude` | number |  |

## Native endpoint

Through the native Atera API, this operation is `GET /api/v3/customers` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/find-customers.md) for the provider-specific parameters and requirements.

