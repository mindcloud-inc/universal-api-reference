# Sertifier: Update Attribute

Updates an existing attribute in Sertifier.

```
PUT https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attributeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-attribute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attributeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributeId` | string | yes | ID of the attribute to update. |
| `title` | string | no | Updated internal title for the attribute. |
| `type` | number | no | Updated attribute value type: 1 text, 2 date, 3 number. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "data": {},
      "hasError": true,
      "isUpgraded": true,
      "message": "string",
      "showPurchaseSheet": true,
      "upgradePlan": {},
      "validationErrors": [
        {
          "key": "string",
          "value": "string"
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
| `content` | object |  |
| `data` | object |  |
| `hasError` | boolean |  |
| `isUpgraded` | boolean |  |
| `message` | string |  |
| `showPurchaseSheet` | boolean |  |
| `upgradePlan` | object |  |
| `validationErrors[].key` | string |  |
| `validationErrors[].value` | string |  |

## Native endpoint

Through the native Sertifier API, this operation is `PUT /attribute/:attributeId` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-attribute.md) for the provider-specific parameters and requirements.

