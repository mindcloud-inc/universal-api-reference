# Ortto: Upsert People



```
POST https://connect.mindcloud.co/v1/universal/ortto/latest/actions/upsert-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/upsert-people" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "people[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ortto/latest/actions/upsert-people', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "people[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `people[]` | array<object> | yes | One or more people to create or update in Ortto. Each item should include a fields object and may include tags or unset_tags. |
| `mergeBy[]` | array<string> | no | Identifiers Ortto should use to match existing people, such as str::email. |
| `async` | boolean | no | Whether Ortto should process the merge asynchronously. |
| `mergeStrategy` | number | no | Ortto merge strategy value to use when matching contacts. |
| `findStrategy` | number | no | Ortto find strategy value to use when creating contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "people": [
        {
          "personId": "string",
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `people[].personId` | string |  |
| `people[].status` | string |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /person/merge` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-people.md) for the provider-specific parameters and requirements.

