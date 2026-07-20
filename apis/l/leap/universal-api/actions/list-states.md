# Leap: List States

Retrieves states for a country from Leap.

```
GET https://connect.mindcloud.co/v1/universal/leap/latest/actions/list-states
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leap/latest/actions/list-states?connectionId=$CONNECTION_ID&countryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leap/latest/actions/list-states?${params}`, {
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
| `countryId` | list | yes | Country to fetch states for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> | List of Leap state records returned by the API. |

## Native endpoint

Through the native Leap API, this operation is `GET /countries/[:countryId]/states` (base URL `https://api.jobprogress.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-states.md) for the provider-specific parameters and requirements.

