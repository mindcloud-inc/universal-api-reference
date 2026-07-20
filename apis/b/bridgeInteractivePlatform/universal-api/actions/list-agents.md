# Bridge Interactive Platform: List agents

Retrieves agent records from Bridge Interactive Platform.

```
GET https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge Interactive Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-agents?connectionId=$CONNECTION_ID&dataset=test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "test"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgeInteractivePlatform/latest/actions/list-agents?${params}`, {
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
| `dataset` | string | yes | Bridge dataset code. This tenant was validated against dataset test. Default: `test`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "MemberEmail": "ava@example.com",
      "MemberFullName": "Ava Chen",
      "MemberKey": "string",
      "MemberMlsId": "string",
      "MemberStatus": "string",
      "OfficeKey": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `MemberEmail` | string |  |
| `MemberFullName` | string |  |
| `MemberKey` | string |  |
| `MemberMlsId` | string |  |
| `MemberStatus` | string |  |
| `OfficeKey` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Bridge Interactive Platform API, this operation is `GET /:dataset/agents` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

