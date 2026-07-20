# GoSquared: List Property Types

Retrieves person property types from GoSquared.

```
GET https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-property-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoSquared `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-property-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/list-property-types?${params}`, {
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
      "manual": true,
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
| `manual` | boolean | Whether the property type was manually created. |
| `name` | string | Provider property name. |
| `type` | string | Provider property data type. |

## Native endpoint

Through the native GoSquared API, this operation is `GET people/v1/propertyTypes` (base URL `https://api.gosquared.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-property-types.md) for the provider-specific parameters and requirements.

