# Currents: Get Affected Test Executions



```
GET https://connect.mindcloud.co/v1/universal/currents/latest/actions/get-affected-test-executions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currents/latest/actions/get-affected-test-executions?connectionId=$CONNECTION_ID&dateEnd=string&dateStart=string&projectId=string&signature=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateEnd": "string",
  "dateStart": "string",
  "projectId": "string",
  "signature": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currents/latest/actions/get-affected-test-executions?${params}`, {
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
| `dateEnd` | string | yes |  |
| `dateStart` | string | yes |  |
| `projectId` | string | yes |  |
| `signature` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "executions": [
          {}
        ],
        "has_more": true
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.executions` | array<object> |  |
| `data.has_more` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Currents API, this operation is `GET /actions/tests/:signature` (base URL `https://api.currents.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-affected-test-executions.md) for the provider-specific parameters and requirements.

