# serviceminder.io: Get Part Dimensions

Retrieves part dimensions from ServiceMinder.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-part-dimensions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-part-dimensions?connectionId=$CONNECTION_ID&partId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "partId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-part-dimensions?${params}`, {
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
| `partId` | number | yes | Part identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dimensions": "string",
      "message": "string",
      "resultCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dimensions` | string |  |
| `message` | string |  |
| `resultCode` | number |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /part/getpartdimensions` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-part-dimensions.md) for the provider-specific parameters and requirements.

