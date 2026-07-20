# Evervault: Retrieve Relay

Retrieves a relay from Evervault.

```
GET https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-relay
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-relay?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evervault/latest/actions/retrieve-relay?${params}`, {
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
      "app": "string",
      "authentication": "string",
      "createdAt": 1,
      "destinationDomain": "string",
      "encryptEmptyStrings": true,
      "evervaultDomain": "string",
      "id": "string",
      "routes": [
        {}
      ],
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | string |  |
| `authentication` | string |  |
| `createdAt` | number |  |
| `destinationDomain` | string |  |
| `encryptEmptyStrings` | boolean |  |
| `evervaultDomain` | string |  |
| `id` | string |  |
| `routes` | array<object> |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Evervault API, this operation is `GET /relays/{id}` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-relay.md) for the provider-specific parameters and requirements.

