# Smoove: Check Contact Exists

Checks whether a contact exists in Smoove.

```
GET https://connect.mindcloud.co/v1/universal/smoove/latest/actions/check-contact-exists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/check-contact-exists?connectionId=$CONNECTION_ID&id=string&by=ContactId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "by": "ContactId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smoove/latest/actions/check-contact-exists?${params}`, {
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
| `id` | string | yes |  |
| `by` | list | yes | One of: `CellPhone`, `ContactId`, `Email`, `ExternalId`. Default: `ContactId`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | boolean |  |

## Native endpoint

Through the native Smoove API, this operation is `GET /v1/Contacts/:id/Exists` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-contact-exists.md) for the provider-specific parameters and requirements.

