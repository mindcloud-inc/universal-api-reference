# MindMe: Update Contact

Updates an existing contact in MindMe.

```
PUT https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/update-contact', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | no |  |
| `companyName` | string | no |  |
| `contactId` | string | no |  |
| `customFieldResponses` | string | no |  |
| `emails` | string | no |  |
| `firstName` | string | no |  |
| `id` | string | no |  |
| `lastName` | string | no |  |
| `listIds` | string | no |  |
| `notes` | string | no |  |
| `parentAccountId` | string | no |  |
| `phones` | string | no |  |
| `tagIds` | string | no |  |
| `timeZoneId` | string | no |  |
| `typeId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MindMe API returns.

## Native endpoint

Through the native MindMe API, this operation is `PUT /api/Contact/UpdateContact` (base URL `https://prodapi.mindmemobile.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

