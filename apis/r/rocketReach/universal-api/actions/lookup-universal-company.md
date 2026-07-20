# RocketReach: Lookup Universal Company

Retrieves a company from RocketReach Universal lookup.

```
GET https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-universal-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RocketReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-universal-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-universal-company?${params}`, {
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
| `domain` | string | no | Domain of the desired company to look up. Preferred identifier. Example: `rocketreach.co`. |
| `id` | number | no | RocketReach internal unique company ID. Example: `123456`. |
| `linkedinUrl` | string | no | LinkedIn URL of the desired company to look up. Example: `www.linkedin.com/company/rocketreach/`. |
| `name` | string | no | Name of the desired company to look up. Example: `RocketReach`. |
| `ticker` | string | no | Stock ticker of the desired company to look up. Example: `MSFT`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RocketReach API returns.

## Native endpoint

Through the native RocketReach API, this operation is `GET /universal/company/lookup` (base URL `https://api.rocketreach.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-universal-company.md) for the provider-specific parameters and requirements.

