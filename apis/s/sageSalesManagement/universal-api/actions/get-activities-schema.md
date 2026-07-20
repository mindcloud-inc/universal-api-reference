# Sage Sales Management: Get Activities Schema

Retrieves the activities schema from Sage Sales Management.

```
GET https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/get-activities-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Sales Management `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/get-activities-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sageSalesManagement/latest/actions/get-activities-schema?${params}`, {
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
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Schema field ID |

## Native endpoint

Through the native Sage Sales Management API, this operation is `GET /activities/schema` (base URL `https://api.forcemanager.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activities-schema.md) for the provider-specific parameters and requirements.

