# RICOH360 Tours: Get Team By API Key



```
GET https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/get-team-by-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RICOH360 Tours `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/get-team-by-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/get-team-by-api-key?${params}`, {
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
        "Type": {
          "fields": [
            {
              "name": "Ava Chen",
              "type": {
                "kind": "string",
                "name": "Ava Chen",
                "ofType": {}
              }
            }
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
| `data.Type.fields[].name` | string |  |
| `data.Type.fields[].type.kind` | string |  |
| `data.Type.fields[].type.name` | string |  |
| `data.Type.fields[].type.ofType` | object |  |

## Native endpoint

Through the native RICOH360 Tours API, this operation is `POST /graphql` (base URL `https://bbomwcm27nhalfwjvwzy6qbrim.appsync-api.us-west-2.amazonaws.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-by-api-key.md) for the provider-specific parameters and requirements.

