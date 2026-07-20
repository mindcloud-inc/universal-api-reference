# Nyckel: List Samples

Retrieves samples from Nyckel.

```
GET https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/list-samples
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyckel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/list-samples?connectionId=$CONNECTION_ID&functionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "functionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/list-samples?${params}`, {
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
| `functionId` | string | yes | Nyckel function identifier. |
| `count` | number | no | Maximum number of samples to return. |
| `startIndex` | number | no | Zero-based sample offset for pagination. |
| `externalId` | string | no | Filter samples by external ID. |
| `annotated` | boolean | no | Filter samples that have annotations. |
| `predicted` | boolean | no | Filter samples that have predictions. |
| `sortBy` | string | no | Sort field. |
| `sortOrder` | string | no | Sort direction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "externalId": "string",
      "id": "string",
      "sampleSets": [
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
| `data` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `sampleSets` | array<object> |  |

## Native endpoint

Through the native Nyckel API, this operation is `GET /functions/:functionId/samples` (base URL `https://www.nyckel.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-samples.md) for the provider-specific parameters and requirements.

