# Tidio: Delete Contact [Plus plan]

Deletes a contact from the Tidio workspace.

```
DELETE https://connect.mindcloud.co/v1/universal/tidio/latest/actions/delete-contact-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/delete-contact-plus-plan?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidio/latest/actions/delete-contact-plus-plan?${params}`, {
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
| `contactId` | string | yes | The Tidio contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. Tidio docs specify 204 It means that the contact has been updated.. |

## Native endpoint

Through the native Tidio API, this operation is `DELETE /contacts/{contactId}` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-plus-plan.md) for the provider-specific parameters and requirements.

