# Nyckel: Get Function Summary

Retrieves a function summary from Nyckel.

```
GET https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/get-function-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyckel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/get-function-summary?connectionId=$CONNECTION_ID&functionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "functionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/get-function-summary?${params}`, {
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
| `functionId` | string | yes | The Nyckel function ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotatedSampleCount": 1,
      "annotatedSampleCountByLabelId": {},
      "sampleCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotatedSampleCount` | number | Annotated samples on the function. |
| `annotatedSampleCountByLabelId` | object | Annotated sample counts grouped by label ID. |
| `sampleCount` | number | Total samples on the function. |

## Native endpoint

Through the native Nyckel API, this operation is `GET /functions/:functionId/summary` (base URL `https://www.nyckel.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-function-summary.md) for the provider-specific parameters and requirements.

