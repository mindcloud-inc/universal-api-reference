# Fidel API: Get MID Request

Retrieves a MID request from Fidel API.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-mid-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-mid-request?connectionId=$CONNECTION_ID&programId=string&midRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "programId": "string",
  "midRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-mid-request?${params}`, {
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
| `programId` | string | yes |  |
| `midRequestId` | string | yes | The MID request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "action": "string",
      "brandId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "estimatedCompletionDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "live": true,
      "locationId": "string",
      "mcAcquiringMid": "string",
      "mcLocationId": "string",
      "origin": "string",
      "programId": "string",
      "result": {},
      "scheme": "string",
      "status": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "visaAcquiringMid": "string",
      "visaBin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `action` | string |  |
| `brandId` | string |  |
| `created` | date |  |
| `estimatedCompletionDate` | date |  |
| `id` | string |  |
| `live` | boolean |  |
| `locationId` | string |  |
| `mcAcquiringMid` | string |  |
| `mcLocationId` | string |  |
| `origin` | string |  |
| `programId` | string |  |
| `result` | object |  |
| `scheme` | string |  |
| `status` | string |  |
| `updated` | date |  |
| `visaAcquiringMid` | string |  |
| `visaBin` | string |  |

## Native endpoint

Through the native Fidel API API, this operation is `GET /programs/:programId/mid-requests/:midRequestId` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mid-request.md) for the provider-specific parameters and requirements.

