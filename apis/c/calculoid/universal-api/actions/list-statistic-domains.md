# Calculoid: List Statistic Domains



```
GET https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-statistic-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-statistic-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-statistic-domains?${params}`, {
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
      "alerts": [
        {
          "msg": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alerts[].msg` | string |  |
| `alerts[].type` | string |  |

## Native endpoint

Through the native Calculoid API, this operation is `GET /statistic/domains` (base URL `https://api.calculoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-statistic-domains.md) for the provider-specific parameters and requirements.

