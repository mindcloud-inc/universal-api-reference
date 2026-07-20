# Microsoft 365 People: List People

Retrieves relevant people from Microsoft 365 People.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 People `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/list-people?${params}`, {
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
      "companyName": "Ava Chen",
      "department": "string",
      "displayName": "Ava Chen",
      "givenName": "Ava",
      "id": "string",
      "jobTitle": "string",
      "officeLocation": "string",
      "personType": {
        "class": "string",
        "subclass": "string"
      },
      "phones": [
        {
          "number": "string",
          "type": "string"
        }
      ],
      "scoredEmailAddresses": [
        {
          "address": "ava@example.com",
          "relevanceScore": 1
        }
      ],
      "surname": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `department` | string |  |
| `displayName` | string |  |
| `givenName` | string |  |
| `id` | string |  |
| `jobTitle` | string |  |
| `officeLocation` | string |  |
| `personType.class` | string |  |
| `personType.subclass` | string |  |
| `phones[].number` | string |  |
| `phones[].type` | string |  |
| `scoredEmailAddresses[].address` | string |  |
| `scoredEmailAddresses[].relevanceScore` | number |  |
| `surname` | string |  |

## Native endpoint

Through the native Microsoft 365 People API, this operation is `GET /v1.0/me/people` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

