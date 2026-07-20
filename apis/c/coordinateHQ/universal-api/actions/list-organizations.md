# CoordinateHQ: List Organizations



```
GET https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoordinateHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/list-organizations?${params}`, {
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
      "entityType": "string",
      "externalObjectId": {},
      "lastModifiedDt": "string",
      "organizationDescription": {},
      "organizationId": "string",
      "organizationName": "Ava Chen",
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entityType` | string |  |
| `externalObjectId` | object |  |
| `lastModifiedDt` | string |  |
| `organizationDescription` | object |  |
| `organizationId` | string |  |
| `organizationName` | string |  |
| `vendorId` | string |  |

## Native endpoint

Through the native CoordinateHQ API, this operation is `GET /organizations` (base URL `https://app.coordinatehq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

