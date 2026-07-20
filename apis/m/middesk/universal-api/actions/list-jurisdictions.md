# Middesk: Fetch supported local jurisdictions

Retrieves supported local jurisdictions from Middesk.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-jurisdictions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-jurisdictions?connectionId=$CONNECTION_ID&state=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "state": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-jurisdictions?${params}`, {
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
| `state` | string | yes | US state abbreviation to fetch supported jurisdictions for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "object": "string",
      "searchConfig": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `object` | string |  |
| `searchConfig` | object |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /agent/jurisdictions` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jurisdictions.md) for the provider-specific parameters and requirements.

