# Socie: Add Additional Field



```
POST https://connect.mindcloud.co/v1/universal/socie/latest/actions/add-additional-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socie/latest/actions/add-additional-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socie/latest/actions/add-additional-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isEditableByMember": true,
      "isMandatoryForMember": true,
      "isVisibleInApp": true,
      "name": "Ava Chen",
      "orderNumber": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the additional field was created in Socie. |
| `id` | string | The Socie additional field id. |
| `isEditableByMember` | boolean | Whether members can edit the field. |
| `isMandatoryForMember` | boolean | Whether members must fill in the field. |
| `isVisibleInApp` | boolean | Whether the field is visible in the Socie app. |
| `name` | string | The additional field name. |
| `orderNumber` | number | The display order for the field. |
| `type` | string | The Socie additional field type. |

## Native endpoint

Through the native Socie API, this operation is `POST /api/v1/additional_fields` (base URL `https://api.socie.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-additional-field.md) for the provider-specific parameters and requirements.

