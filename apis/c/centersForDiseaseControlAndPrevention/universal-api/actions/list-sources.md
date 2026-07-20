# Centers for Disease Control and Prevention: List Sources

Retrieves sources from CDC Content Services.

```
GET https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/list-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centers for Disease Control and Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/list-sources?${params}`, {
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
      "acronym": "string",
      "largeLogoUrl": "https://example.com",
      "name": "Ava Chen",
      "smallLogoUrl": "https://example.com",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acronym` | string |  |
| `largeLogoUrl` | string |  |
| `name` | string |  |
| `smallLogoUrl` | string |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Centers for Disease Control and Prevention API, this operation is `GET /v2/resources/sources` (base URL `https://tools.cdc.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sources.md) for the provider-specific parameters and requirements.

