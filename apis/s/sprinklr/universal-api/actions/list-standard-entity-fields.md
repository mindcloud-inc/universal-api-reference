# Sprinklr: List Standard Entity Fields

Retrieves standard entity fields from Sprinklr.

```
GET https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/list-standard-entity-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sprinklr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/list-standard-entity-fields?connectionId=$CONNECTION_ID&entityType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/list-standard-entity-fields?${params}`, {
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
| `entityType` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiName": "Ava Chen",
      "entityDefinitionId": "string",
      "id": "string",
      "multivalued": true,
      "name": "Ava Chen",
      "picklistValues": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiName` | string |  |
| `entityDefinitionId` | string |  |
| `id` | string |  |
| `multivalued` | boolean |  |
| `name` | string |  |
| `picklistValues` | array |  |
| `type` | string |  |

## Native endpoint

Through the native Sprinklr API, this operation is `GET api/v2/standard-entity/fields/{entityType}` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-standard-entity-fields.md) for the provider-specific parameters and requirements.

