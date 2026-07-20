# Ubiqod by Skiply: Add Codes To PIN Code List



```
PUT https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/add-codes-to-pin-code-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubiqod by Skiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/add-codes-to-pin-code-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pinCodeListId": "string",
  "list[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/add-codes-to-pin-code-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pinCodeListId": "string",
    "list[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pinCodeListId` | string | yes | PIN code list ID. |
| `list[]` | array<object> | yes | PIN codes to add to the list. |

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

Through the native Ubiqod by Skiply API, this operation is `POST /pincodes/:pinCodeListId/codes` (base URL `https://api.ubiqod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-codes-to-pin-code-list.md) for the provider-specific parameters and requirements.

