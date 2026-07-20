# OneMap SG: Convert WGS84 to SVY21

Converts WGS84 coordinates to SVY21 in OneMap SG.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/convert4326-to3414
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/convert4326-to3414?connectionId=$CONNECTION_ID&latitude=1.319728905&longitude=103.8421581" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "1.319728905",
  "longitude": "103.8421581"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/convert4326-to3414?${params}`, {
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
| `latitude` | number | yes | The WGS84 latitude value. Example: `1.319728905`. |
| `longitude` | number | yes | The WGS84 longitude value. Example: `103.8421581`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "X": 1,
      "Y": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `X` | number |  |
| `Y` | number |  |

## Native endpoint

Through the native OneMap SG API, this operation is `GET /api/common/convert/4326to3414` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert4326-to3414.md) for the provider-specific parameters and requirements.

