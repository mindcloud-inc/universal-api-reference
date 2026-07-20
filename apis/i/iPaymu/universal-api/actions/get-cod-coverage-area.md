# iPaymu: Get COD Coverage Area

Check whether a location is covered by iPaymu cash-on-delivery service.

```
GET https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/get-cod-coverage-area
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iPaymu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/get-cod-coverage-area?connectionId=$CONNECTION_ID&area=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "area": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/get-cod-coverage-area?${params}`, {
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
| `area` | string | yes | Area search text with at least three characters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cityName": "Ava Chen",
      "districtName": "Ava Chen",
      "id": 1,
      "label": "string",
      "provinceName": "Ava Chen",
      "subdistrictName": "Ava Chen",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cityName` | string |  |
| `districtName` | string |  |
| `id` | number |  |
| `label` | string |  |
| `provinceName` | string |  |
| `subdistrictName` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native iPaymu API, this operation is `GET /cod/area` (base URL `https://my.ipaymu.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cod-coverage-area.md) for the provider-specific parameters and requirements.

