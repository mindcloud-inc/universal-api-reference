# Tellephant: Update contact tags

Updates tags for WhatsApp contacts in Tellephant.

```
PUT https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/update-contact-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tellephant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/update-contact-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/update-contact-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array<object> | yes | Array of contact tag update objects with contact_id and tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tellephant API, this operation is `PATCH /v1/user/tags/update` (base URL `https://api.tellephant.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-tags.md) for the provider-specific parameters and requirements.

