# Fibery: Get Schema

Retrieves a schema from Fibery.

```
GET https://connect.mindcloud.co/v1/universal/fibery/latest/actions/get-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fibery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/get-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fibery/latest/actions/get-schema?${params}`, {
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
| `args.withDescription` | boolean | no | Include type descriptions in the schema response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "fibery/id": "string",
        "fibery/meta": {
          "fibery/rel-version": "string",
          "fibery/version": "string"
        },
        "fibery/types": [
          {
            "fibery/deleted?": true,
            "fibery/fields": [
              {
                "fibery/deleted?": true,
                "fibery/id": "string",
                "fibery/meta": {
                  "fibery/id?": true,
                  "fibery/readonly?": true,
                  "fibery/required?": true,
                  "fibery/secured?": true
                },
                "fibery/name": "Ava Chen",
                "fibery/type": "string"
              }
            ],
            "fibery/id": "string",
            "fibery/meta": {
              "fibery/domain?": true,
              "fibery/platform?": true,
              "fibery/primitive?": true,
              "fibery/secured?": true,
              "ui/color": "string"
            },
            "fibery/name": "Ava Chen"
          }
        ],
        "fibery/version": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.fibery/id` | string |  |
| `result.fibery/meta.fibery/rel-version` | string |  |
| `result.fibery/meta.fibery/version` | string |  |
| `result.fibery/types[].fibery/deleted?` | boolean |  |
| `result.fibery/types[].fibery/fields[].fibery/deleted?` | boolean |  |
| `result.fibery/types[].fibery/fields[].fibery/id` | string |  |
| `result.fibery/types[].fibery/fields[].fibery/meta.fibery/id?` | boolean |  |
| `result.fibery/types[].fibery/fields[].fibery/meta.fibery/readonly?` | boolean |  |
| `result.fibery/types[].fibery/fields[].fibery/meta.fibery/required?` | boolean |  |
| `result.fibery/types[].fibery/fields[].fibery/meta.fibery/secured?` | boolean |  |
| `result.fibery/types[].fibery/fields[].fibery/name` | string |  |
| `result.fibery/types[].fibery/fields[].fibery/type` | string |  |
| `result.fibery/types[].fibery/id` | string |  |
| `result.fibery/types[].fibery/meta.fibery/domain?` | boolean |  |
| `result.fibery/types[].fibery/meta.fibery/platform?` | boolean |  |
| `result.fibery/types[].fibery/meta.fibery/primitive?` | boolean |  |
| `result.fibery/types[].fibery/meta.fibery/secured?` | boolean |  |
| `result.fibery/types[].fibery/meta.ui/color` | string |  |
| `result.fibery/types[].fibery/name` | string |  |
| `result.fibery/version` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Fibery API, this operation is `POST /commands` (base URL `https://{{credentials.account}}.fibery.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schema.md) for the provider-specific parameters and requirements.

