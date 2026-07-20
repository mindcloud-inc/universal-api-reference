# Mixpanel: Update Group Property

Updates a group property in Mixpanel.

```
PUT https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/update-group-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/update-group-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupKey": "company",
  "groupId": "acme",
  "set": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/update-group-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupKey": "company",
    "groupId": "acme",
    "set": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupKey` | string | yes | Group key that identifies the type of group profile to update. Example: `company`. |
| `groupId` | string | yes | ID of the specific group profile to update. Example: `acme`. |
| `set` | object | yes | Object of group profile properties to set. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ip` | number | no | Set to 1 to use the request IP for geolocation updates. Example: `1`. |
| `strict` | number | no | Set to 1 to return validation errors for invalid updates. Example: `1`. |
| `verbose` | number | no | Set to 1 to include verbose validation messages in the response. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | number | Mixpanel group ingestion success flag where 1 indicates success and 0 indicates failure. |

## Native endpoint

Through the native Mixpanel API, this operation is `POST https://api.mixpanel.com/groups` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group-property.md) for the provider-specific parameters and requirements.

