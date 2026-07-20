# Sprinklr: Get Standard Entity Definition

Retrieves a standard entity definition from Sprinklr.

```
GET https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/get-standard-entity-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sprinklr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/get-standard-entity-definition?connectionId=$CONNECTION_ID&entityType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/get-standard-entity-definition?${params}`, {
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
| `createdTime` | number |  |
| `id` | string |  |
| `modifiedTime` | number |  |
| `name` | string |  |
| `pluralName` | string |  |

## Native endpoint

Through the native Sprinklr API, this operation is `GET api/v2/standard-entity/definition/{entityType}` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-standard-entity-definition.md) for the provider-specific parameters and requirements.

