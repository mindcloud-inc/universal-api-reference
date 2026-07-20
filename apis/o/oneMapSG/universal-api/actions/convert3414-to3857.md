# OneMap SG: Convert SVY21 to EPSG:3857

Converts SVY21 coordinates to EPSG:3857 in OneMap SG.

```
GET https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/convert3414-to3857
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/convert3414-to3857?connectionId=$CONNECTION_ID&x=28983.788791079794&y=33554.509813284" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "x": "28983.788791079794",
  "y": "33554.509813284"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/convert3414-to3857?${params}`, {
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
| `x` | number | yes | The SVY21 X coordinate. Example: `28983.788791079794`. |
| `y` | number | yes | The SVY21 Y coordinate. Example: `33554.509813284`. |

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

Through the native OneMap SG API, this operation is `GET /api/common/convert/3414to3857` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert3414-to3857.md) for the provider-specific parameters and requirements.

