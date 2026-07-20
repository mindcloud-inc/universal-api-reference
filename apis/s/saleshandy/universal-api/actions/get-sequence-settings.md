# Saleshandy: Get Sequence Settings



```
GET https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/get-sequence-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saleshandy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/get-sequence-settings?connectionId=$CONNECTION_ID&sequenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sequenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/get-sequence-settings?${params}`, {
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
| `sequenceId` | string | yes | Sequence ID to fetch settings for. |
| `code` | number | no | Optional settings code to filter the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "payload": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `payload` | object |  |

## Native endpoint

Through the native Saleshandy API, this operation is `GET /sequences/[:sequenceId]/settings` (base URL `https://open-api.saleshandy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sequence-settings.md) for the provider-specific parameters and requirements.

