# Intruder: List Licenses



```
GET https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-licenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-licenses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-licenses?${params}`, {
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
      "availableApplicationLicenses": 1,
      "availableInfrastructureLicenses": 1,
      "consumedApplicationLicenses": 1,
      "consumedInfrastructureLicenses": 1,
      "totalApplicationLicenses": 1,
      "totalInfrastructureLicenses": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableApplicationLicenses` | number |  |
| `availableInfrastructureLicenses` | number |  |
| `consumedApplicationLicenses` | number |  |
| `consumedInfrastructureLicenses` | number |  |
| `totalApplicationLicenses` | number |  |
| `totalInfrastructureLicenses` | number |  |

## Native endpoint

Through the native Intruder API, this operation is `GET /licenses/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-licenses.md) for the provider-specific parameters and requirements.

