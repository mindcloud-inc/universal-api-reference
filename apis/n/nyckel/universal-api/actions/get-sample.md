# Nyckel: Get Sample

Retrieves a sample from Nyckel.

```
GET https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/get-sample
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyckel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/get-sample?connectionId=$CONNECTION_ID&functionId=string&sampleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "functionId": "string",
  "sampleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/get-sample?${params}`, {
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
| `sampleId` | string | yes | Nyckel sample identifier. |

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

Through the native Nyckel API, this operation is `GET /functions/:functionId/samples/:sampleId` (base URL `https://www.nyckel.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sample.md) for the provider-specific parameters and requirements.

