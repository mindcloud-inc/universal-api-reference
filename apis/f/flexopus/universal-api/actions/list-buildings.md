# Flexopus: List Buildings

Retrieves a list of buildings from Flexopus.

```
GET https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-buildings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-buildings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-buildings?${params}`, {
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
      "data": [
        {
          "address": "string",
          "id": 1,
          "locations": [
            {
              "code": "string",
              "id": 1,
              "name": "Ava Chen"
            }
          ],
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].address` | string |  |
| `data[].id` | number |  |
| `data[].locations` | array<object> |  |
| `data[].locations[].code` | string |  |
| `data[].locations[].id` | number |  |
| `data[].locations[].name` | string |  |
| `data[].name` | string |  |

## Native endpoint

Through the native Flexopus API, this operation is `GET /buildings` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-buildings.md) for the provider-specific parameters and requirements.

