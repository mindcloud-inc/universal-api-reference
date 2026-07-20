# City of Beverly Hills: List Services

Retrieves ArcGIS service records from City of Beverly Hills.

```
GET https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a City of Beverly Hills `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfBeverlyHills/latest/actions/list-services?${params}`, {
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
      "currentVersion": 1,
      "services": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentVersion` | number | ArcGIS REST API version for the services directory response. |
| `services[]` | array<object> | List of service records exposed by the directory. |
| `services[].name` | string | Service name. |
| `services[].type` | string | Service type. |
| `services[].url` | string | Fully qualified service URL. |

## Native endpoint

Through the native City of Beverly Hills API, this operation is `GET services` (base URL `https://services5.arcgis.com/7CXE3aevo18HlHBC/arcgis/rest/services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

