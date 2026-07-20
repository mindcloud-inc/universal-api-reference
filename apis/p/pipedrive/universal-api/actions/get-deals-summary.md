# Pipedrive: Get Deals Summary

Retrieves deal summary metrics from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-deals-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-deals-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-deals-summary?${params}`, {
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
| `status` | string | no | Filter by status: open, won, or lost. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalCount` | number |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v1/deals/summary` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deals-summary.md) for the provider-specific parameters and requirements.

