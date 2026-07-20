# Wooxy: Get Contact

Retrieves a contact from your Wooxy account.

```
GET https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactListId=yourContactListId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactListId": "yourContactListId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-contact?${params}`, {
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
| `contactListId` | string | yes | Wooxy contact list ID. Example: `yourContactListId`. |
| `email` | string | no | Contact email address. Example: `user@example.com`. |
| `phoneNumber` | string | no | Contact phone number in E.164 format. Example: `+15555555555`. |
| `userId` | string | no | Contact user ID. Example: `stageThreeUser`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wooxy API returns.

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/contact/get` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

