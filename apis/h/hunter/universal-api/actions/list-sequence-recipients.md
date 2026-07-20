# Hunter: List Sequence Recipients



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/list-sequence-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/list-sequence-recipients?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/list-sequence-recipients?${params}`, {
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
| `campaignId` | string | yes | Identifier of the sequence. |
| `limit` | number | no |  |
| `offset` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recipients": [
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
| `recipients` | array<object> | Recipients already added to the sequence. |

## Native endpoint

Through the native Hunter API, this operation is `GET /campaigns/:campaignId/recipients` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sequence-recipients.md) for the provider-specific parameters and requirements.

