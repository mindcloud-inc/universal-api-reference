# Avoma: List Meeting Outcomes

Retrieves meeting outcomes from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-meeting-outcomes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-meeting-outcomes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-meeting-outcomes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "label": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `label` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/meeting_outcome/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-meeting-outcomes.md) for the provider-specific parameters and requirements.

