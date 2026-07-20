# Sprinklr: List Custom Entity Definitions

Retrieves custom entity definitions from Sprinklr.

```
GET https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/list-custom-entity-definitions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sprinklr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/list-custom-entity-definitions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/list-custom-entity-definitions?${params}`, {
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
      "createdTime": 1,
      "id": "string",
      "modifiedTime": 1,
      "name": "Ava Chen",
      "pluralName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | number | Created time for the custom entity definition. |
| `id` | string | Custom entity definition ID. |
| `modifiedTime` | number | Last modified time for the custom entity definition. |
| `name` | string | Custom entity definition name. |
| `pluralName` | string | Plural name for the custom entity definition. |

## Native endpoint

Through the native Sprinklr API, this operation is `GET api/v2/custom-entity/definitions` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-entity-definitions.md) for the provider-specific parameters and requirements.

