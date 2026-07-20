# Hygraph: Introspect Schema

Retrieves GraphQL schema details from Hygraph.

```
GET https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/introspect-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hygraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/introspect-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/introspect-schema?${params}`, {
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
      "data": {
        "__schema": {
          "mutationType": {},
          "queryType": {},
          "types": [
            {}
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.__schema` | object | Hygraph GraphQL schema introspection object. |
| `data.__schema.mutationType` | object | Schema mutation root type. |
| `data.__schema.queryType` | object | Schema query root type. |
| `data.__schema.types` | array<object> | GraphQL schema types. |

## Native endpoint

Through the native Hygraph API, this operation is `POST` (base URL `{{credentials.endpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/introspect-schema.md) for the provider-specific parameters and requirements.

