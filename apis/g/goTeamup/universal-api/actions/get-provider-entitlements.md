# GoTeamup: Get Provider Entitlements

Retrieves provider entitlements from GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/get-provider-entitlements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/get-provider-entitlements?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/get-provider-entitlements?${params}`, {
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
| `id` | number | yes | The TeamUp provider ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customBrandedApp": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customBrandedApp` | boolean |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /providers/:id/entitlements` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-provider-entitlements.md) for the provider-specific parameters and requirements.

