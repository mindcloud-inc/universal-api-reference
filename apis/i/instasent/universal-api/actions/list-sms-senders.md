# Instasent: List SMS Senders



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-sms-senders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-sms-senders?connectionId=$CONNECTION_ID&project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/list-sms-senders?${params}`, {
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
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {
        "count": 1,
        "defaultSender": {},
        "limit": 1,
        "start": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata.count` | number |  |
| `metadata.defaultSender` | object |  |
| `metadata.limit` | number |  |
| `metadata.start` | number |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/channel/sms/sender` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sms-senders.md) for the provider-specific parameters and requirements.

