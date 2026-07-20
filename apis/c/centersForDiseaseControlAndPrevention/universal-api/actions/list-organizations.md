# Centers for Disease Control and Prevention: List Organizations

Retrieves organizations from CDC Content Services.

```
GET https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centers for Disease Control and Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/list-organizations?${params}`, {
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
      "address": "string",
      "city": "string",
      "country": "string",
      "county": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "postalCode": "string",
      "stateProvince": "string",
      "type": "string",
      "typeOther": "string",
      "website": [
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
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `county` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `postalCode` | string |  |
| `stateProvince` | string |  |
| `type` | string |  |
| `typeOther` | string |  |
| `website` | array<object> |  |

## Native endpoint

Through the native Centers for Disease Control and Prevention API, this operation is `GET /v2/resources/organizations` (base URL `https://tools.cdc.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

