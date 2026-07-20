# Bokun: List Experience IDs

Retrieves owned experience product IDs from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-ids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-ids?${params}`, {
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
| `activated` | boolean | no | Optional flag to filter activated experience IDs only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/experiences/ids` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-experience-ids.md) for the provider-specific parameters and requirements.

