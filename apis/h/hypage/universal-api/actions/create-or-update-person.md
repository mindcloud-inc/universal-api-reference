# Hy.page: Create or Update Person



```
PUT https://connect.mindcloud.co/v1/universal/hypage/latest/actions/create-or-update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/create-or-update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hypage/latest/actions/create-or-update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `city` | string | no | City. |
| `country` | string | no | Country. |
| `email` | string | yes | Trimmed, lowercased person email. |
| `notes` | string | no | Notes stored in metadata. |
| `phone` | string | no | Phone number. |
| `referrer` | string | no | Referrer URL, max 1000 characters. |
| `state` | string | no | State. |
| `utmSource` | string | no | UTM source, max 200 characters. |
| `name` | string | no | Display name. |
| `tags` | string | no | Tags merged with existing tags on update. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaseValue` | number | no | Purchase value. Validation error if NaN. |
| `source` | string | no | Signup source. Defaults to API on create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "isNew": true,
      "metadata": {},
      "name": "Ava Chen",
      "purchaseValue": 1,
      "signupSource": "string",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | string |  |
| `isNew` | boolean |  |
| `metadata` | object |  |
| `name` | string |  |
| `purchaseValue` | number |  |
| `signupSource` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Hy.page API, this operation is `POST /hyax-api/v1/people/add` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-person.md) for the provider-specific parameters and requirements.

