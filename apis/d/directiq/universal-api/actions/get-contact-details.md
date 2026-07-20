# DirectIQ: Get contact details

Retrieves detailed contact information from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-contact-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-contact-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-contact-details?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "keys": [
        [
          {}
        ]
      ],
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `keys[]` | array<object> |  |
| `keys[].dateFormat` | string |  |
| `keys[].keyId` | number |  |
| `keys[].keyName` | string |  |
| `keys[].keyType` | number |  |
| `keys[].keyValue` | string |  |
| `keys[].keyValueDate` | date |  |
| `keys[].keyValueNumber` | number |  |
| `lastName` | string |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /contacts/contactdetails/get/{id}` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-details.md) for the provider-specific parameters and requirements.

