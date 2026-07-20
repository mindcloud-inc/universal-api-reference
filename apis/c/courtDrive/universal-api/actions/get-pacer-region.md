# Court Drive: Get PACER Region



```
GET https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-pacer-region
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Court Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-pacer-region?connectionId=$CONNECTION_ID&regionCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "regionCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/courtDrive/latest/actions/get-pacer-region?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `regionCode` | string | yes | PACER region code to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "links": {},
      "name": "Ava Chen",
      "parent_code": "string",
      "parent_regions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `links` | object |  |
| `name` | string |  |
| `parent_code` | string |  |
| `parent_regions` | array<object> |  |

## Native endpoint

Through the native Court Drive API, this operation is `GET /regions/pacer/{region_code}` (base URL `https://v1.courtapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pacer-region.md) for the provider-specific parameters and requirements.

