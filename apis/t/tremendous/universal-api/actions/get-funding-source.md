# Tremendous: Retrieve Funding Source

Retrieves a specific funding source from Tremendous.

```
GET https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/get-funding-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tremendous `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/get-funding-source?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/get-funding-source?${params}`, {
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
| `id` | string | yes | ID of the funding source to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "funding_source": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `funding_source` | object |  |

## Native endpoint

Through the native Tremendous API, this operation is `GET /funding_sources/:id` (base URL `https://testflight.tremendous.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-funding-source.md) for the provider-specific parameters and requirements.

