# Sipuni: Export All Statistics

Exports all call recording entries from Sipuni.

```
GET https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/export-all-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sipuni `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/export-all-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/export-all-statistics?${params}`, {
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
| `limit` | string | no | Maximum 200000 rows per page. Default: `200000`. |
| `order` | string | no | Use asc to count from earliest rows or desc from latest rows. Default: `asc`. |
| `page` | string | no | Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw CSV response returned by Sipuni. |

## Native endpoint

Through the native Sipuni API, this operation is `GET /statistic/export/all` (base URL `https://sipuni.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-all-statistics.md) for the provider-specific parameters and requirements.

