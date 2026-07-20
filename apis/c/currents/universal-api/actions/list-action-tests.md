# Currents: List Action Tests



```
GET https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-action-tests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-action-tests?connectionId=$CONNECTION_ID&actionId=string&dateStart=string&dateEnd=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionId": "string",
  "dateStart": "string",
  "dateEnd": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-action-tests?${params}`, {
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
| `actionId` | string | yes |  |
| `dateStart` | string | yes | Start date in ISO 8601 format. |
| `dateEnd` | string | yes | End date in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Currents API, this operation is `GET /actions/:actionId/tests` (base URL `https://api.currents.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-action-tests.md) for the provider-specific parameters and requirements.

