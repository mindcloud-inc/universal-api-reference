# Affinda: Get usage by workspace

Retrieves monthly credits usage for an Affinda workspace.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-workspace-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-workspace-usage?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/get-workspace-usage?${params}`, {
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
| `end` | string | no | End date of the period to retrieve. Format: YYYY-MM |
| `identifier` | string | yes | Workspace's identifier |
| `start` | string | no | Start date of the period to retrieve. Format: YYYY-MM |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "month": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `month` | string |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/workspaces/:identifier/usage` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-usage.md) for the provider-specific parameters and requirements.

