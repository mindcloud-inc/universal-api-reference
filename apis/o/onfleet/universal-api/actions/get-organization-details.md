# Onfleet: Get Organization Details

Retrieves your organization's details from Onfleet.

```
GET https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-organization-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-organization-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-organization-details?${params}`, {
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
      "country": "string",
      "delegatees": [
        "string"
      ],
      "driverSupportEmail": "ava@example.com",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `delegatees` | array |  |
| `driverSupportEmail` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Onfleet API, this operation is `GET /organization` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-details.md) for the provider-specific parameters and requirements.

