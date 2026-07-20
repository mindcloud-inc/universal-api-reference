# Ubiqod by Skiply: Create PIN Code List



```
POST https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/create-pin-code-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubiqod by Skiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/create-pin-code-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "string",
  "list[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/create-pin-code-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "string",
    "list[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | yes | PIN code list label. |
| `list[]` | array<object> | yes | PIN codes to include in the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "list": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | PIN code list ID. |
| `label` | string | PIN code list label. |
| `list` | array<object> | PIN codes in the list. |

## Native endpoint

Through the native Ubiqod by Skiply API, this operation is `POST /pincodes/` (base URL `https://api.ubiqod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pin-code-list.md) for the provider-specific parameters and requirements.

