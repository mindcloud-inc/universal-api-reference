# Previsto: List Organizations

Retrieves organizations from Previsto.

```
GET https://connect.mindcloud.co/v1/universal/previsto/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Previsto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/previsto/latest/actions/list-organizations?${params}`, {
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
      "address": "string",
      "apiVersion": "string",
      "appartment": {},
      "baseCurrency": "string",
      "city": "string",
      "countryCode": "string",
      "createdBy": "string",
      "createdDate": "string",
      "email": "ava@example.com",
      "id": "string",
      "languageCode": "string",
      "lastModifiedBy": "string",
      "lastModifiedDate": "string",
      "location": [
        1
      ],
      "name": "Ava Chen",
      "phone": {},
      "postalCode": "string",
      "registrationNo": {},
      "taxRates": [
        {
          "rate": 1,
          "workType": "string"
        }
      ],
      "timeZone": "string",
      "url": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `apiVersion` | string |  |
| `appartment` | object |  |
| `baseCurrency` | string |  |
| `city` | string |  |
| `countryCode` | string |  |
| `createdBy` | string |  |
| `createdDate` | string |  |
| `email` | string |  |
| `id` | string |  |
| `languageCode` | string |  |
| `lastModifiedBy` | string |  |
| `lastModifiedDate` | string |  |
| `location[]` | number |  |
| `name` | string |  |
| `phone` | object |  |
| `postalCode` | string |  |
| `registrationNo` | object |  |
| `taxRates[].rate` | number |  |
| `taxRates[].workType` | string |  |
| `timeZone` | string |  |
| `url` | object |  |

## Native endpoint

Through the native Previsto API, this operation is `GET /organizations` (base URL `https://api.previsto.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

