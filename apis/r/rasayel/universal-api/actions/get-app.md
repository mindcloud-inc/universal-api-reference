# Rasayel: Get App

Retrieves the current Rasayel workspace details.

```
GET https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/get-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rasayel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/get-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/get-app?${params}`, {
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
      "companyDomain": "string",
      "createdAt": 1,
      "displayName": "Ava Chen",
      "id": 1,
      "updatedAt": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyDomain` | string |  |
| `createdAt` | number |  |
| `displayName` | string |  |
| `id` | number |  |
| `updatedAt` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Rasayel API, this operation is `POST /` (base URL `https://api.rasayel.io/api/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app.md) for the provider-specific parameters and requirements.

