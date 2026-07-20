# Formitize: List Clients

Retrieves clients from Formitize.

```
GET https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-clients?${params}`, {
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
      "billingName": "Ava Chen",
      "cachedata": [
        {}
      ],
      "clientID": "string",
      "clientType": "string",
      "contactID": "string",
      "dateCreated": "string",
      "dateModified": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "latestNote": "string",
      "name": "Ava Chen",
      "primaryAddress": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingName` | string |  |
| `cachedata` | array<object> |  |
| `clientID` | string |  |
| `clientType` | string |  |
| `contactID` | string |  |
| `dateCreated` | string |  |
| `dateModified` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `latestNote` | string |  |
| `name` | string |  |
| `primaryAddress` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Formitize API, this operation is `GET /crm/client/list/` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

