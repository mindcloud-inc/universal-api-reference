# BetterContact: Get Lead Finder Search Results

Retrieves BetterContact lead finder search results by request ID.

```
GET https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/get-lead-finder-search-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BetterContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/get-lead-finder-search-results?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/get-lead-finder-search-results?${params}`, {
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
| `requestId` | string | yes | The BetterContact lead finder request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": "string",
      "creditsLeft": "string",
      "id": "string",
      "status": "string",
      "summary": {
        "leadsFound": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | string |  |
| `creditsLeft` | string |  |
| `id` | string |  |
| `status` | string |  |
| `summary.leadsFound` | number |  |

## Native endpoint

Through the native BetterContact API, this operation is `GET /lead_finder/async/:request_id` (base URL `https://app.bettercontact.rocks/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-finder-search-results.md) for the provider-specific parameters and requirements.

