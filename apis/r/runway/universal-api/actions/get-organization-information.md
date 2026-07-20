# Runway: Get Organization Information

Retrieves organization information from Runway.

```
GET https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-organization-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-organization-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-organization-information?${params}`, {
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
      "creditBalance": 1,
      "tier": {},
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditBalance` | number |  |
| `tier` | object |  |
| `usage` | object |  |

## Native endpoint

Through the native Runway API, this operation is `GET /v1/organization` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-information.md) for the provider-specific parameters and requirements.

