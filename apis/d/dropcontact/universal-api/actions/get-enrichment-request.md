# Dropcontact: Get Enrichment Request

Retrieves contact enrichment results from Dropcontact.

```
GET https://connect.mindcloud.co/v1/universal/dropcontact/latest/actions/get-enrichment-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropcontact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropcontact/latest/actions/get-enrichment-request?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropcontact/latest/actions/get-enrichment-request?${params}`, {
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
| `forceResults` | boolean | no | Return partial results even if processing is still running. |
| `requestId` | string | yes | Request ID returned by the enrich POST call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_left": 1,
      "data": [
        {}
      ],
      "error": true,
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_left` | number |  |
| `data` | array<object> |  |
| `error` | boolean |  |
| `status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Dropcontact API, this operation is `GET /v1/enrich/all/{{requestId}}` (base URL `https://api.dropcontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enrichment-request.md) for the provider-specific parameters and requirements.

