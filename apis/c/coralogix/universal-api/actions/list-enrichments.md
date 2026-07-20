# Coralogix: List Enrichments



```
GET https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-enrichments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coralogix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-enrichments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/list-enrichments?${params}`, {
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
      "enrichments": [
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
| `enrichments` | array<object> | enrichments returned by Coralogix. |

## Native endpoint

Through the native Coralogix API, this operation is `GET /enrichment-rules/enrichment-rules/v1` (base URL `https://api.eu2.coralogix.com/mgmt/openapi/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-enrichments.md) for the provider-specific parameters and requirements.

