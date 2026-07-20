# Interzoid: Compare Full Names



```
GET https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/compare-full-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Interzoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/compare-full-names?connectionId=$CONNECTION_ID&fullname1=Ava%20Chen&fullname2=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fullname1": "Ava Chen",
  "fullname2": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/compare-full-names?${params}`, {
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
| `fullname1` | string | yes | First full name. |
| `fullname2` | string | yes | Second full name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": "string",
      "Credits": "string",
      "Score": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string |  |
| `Credits` | string |  |
| `Score` | string |  |

## Native endpoint

Through the native Interzoid API, this operation is `GET /getfullnamematchscore` (base URL `https://api.interzoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-full-names.md) for the provider-specific parameters and requirements.

