# Samsara: Get Organization



```
GET https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-organization?${params}`, {
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
      "carrierSettings": {
        "carrierName": "Ava Chen",
        "dotNumber": 1,
        "mainOfficeAddress": "string"
      },
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrierSettings.carrierName` | string |  |
| `carrierSettings.dotNumber` | number |  |
| `carrierSettings.mainOfficeAddress` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Samsara API, this operation is `GET me` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

