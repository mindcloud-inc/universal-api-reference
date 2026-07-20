# SparkPost: Retrieve Suppression



```
GET https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-suppression
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-suppression?connectionId=$CONNECTION_ID&recipient=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recipient": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-suppression?${params}`, {
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
| `recipient` | string | yes | Suppressed recipient email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "description": "string",
      "recipient": "string",
      "source": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `description` | string |  |
| `recipient` | string |  |
| `source` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SparkPost API, this operation is `GET /suppression-list/:recipient` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-suppression.md) for the provider-specific parameters and requirements.

