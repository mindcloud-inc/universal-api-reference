# Starburst Galaxy: Get Cassandra catalog



```
GET https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-cassandra-catalog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starburst Galaxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-cassandra-catalog?connectionId=$CONNECTION_ID&catalogId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "catalogId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-cassandra-catalog?${params}`, {
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
| `catalogId` | string | yes | Starburst Galaxy catalog ID. Docs also support URL-encoded lookup expressions such as name=value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "catalogId": "string",
      "description": "string",
      "name": "Ava Chen",
      "readOnly": true,
      "validate": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `catalogId` | string |  |
| `description` | string |  |
| `name` | string |  |
| `readOnly` | boolean |  |
| `validate` | boolean |  |

## Native endpoint

Through the native Starburst Galaxy API, this operation is `GET /public/api/v1/catalogType/cassandra/catalog/{catalogId}` (base URL `https://mindcloud.galaxy.starburst.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cassandra-catalog.md) for the provider-specific parameters and requirements.

