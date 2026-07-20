# Namsor: Software Version

Retrieves the current Namsor software version.

```
GET https://connect.mindcloud.co/v1/universal/namsor/latest/actions/software-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Namsor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/software-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/namsor/latest/actions/software-version?${params}`, {
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
      "softwareNameAndVersion": "Ava Chen",
      "softwareVersion": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `softwareNameAndVersion` | string |  |
| `softwareVersion` | array<number> |  |

## Native endpoint

Through the native Namsor API, this operation is `GET /api2/json/softwareVersion` (base URL `https://v2.namsor.com/NamSorAPIv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/software-version.md) for the provider-specific parameters and requirements.

