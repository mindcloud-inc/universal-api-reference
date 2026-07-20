# Recombee: Get User Property Info

Retrieves details for a user property in Recombee.

```
GET https://connect.mindcloud.co/v1/universal/recombee/latest/actions/get-user-property-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recombee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/get-user-property-info?connectionId=$CONNECTION_ID&propertyName=country" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyName": "country"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recombee/latest/actions/get-user-property-info?${params}`, {
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
| `propertyName` | string | yes | Example: `country`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Property name returned by Recombee. |
| `type` | string | Property data type returned by Recombee. |

## Native endpoint

Through the native Recombee API, this operation is `GET /users/properties/:propertyName` (base URL `https://rapi.recombee.com/{{credentials.databaseId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-property-info.md) for the provider-specific parameters and requirements.

